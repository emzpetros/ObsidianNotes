# Changing Levels
The PW of the stim output is modulated along two lines
- PW threshold to PWref and PWref to PWmax
- ***Level modulates PW Ref***

Below processing is done for each location (heel, midfoot, toes)


## Checks on Raw Level Values
Levels set as *lev / 100*
Corrected to 0.2 or -0.2 as needed if somehow set beyond the range of the sliders 
Range check on PWref: setLevelLimMin = 0.05
```
// safety check: check that level setting doesn't place PWref within certain % of PWmin and PWmax
    else if (((1 + levelFloat) * pwRef) <= ((1 + setLevelLimMin) * pwMin))
    {
        level = (((1 + setLevelLimMin) * pwMin) / pwRef) - 1;
    }   
```

## Creation of Lines
![[Pasted image 20231030111330.png]]

```
void EqnParams::create_lines()
{
    line1.Vstart = Vth;
    line1.Vend = Vref;
    line1.m = ((pwRef * (1 + level)) - pwMin) / (Vref - Vth);
    line1.b = pwMin - (Vth * line1.m);

    line2.Vstart = Vref;
    line2.Vend = Vmax;
    line2.m = (pwMax - (pwRef * (1 + level))) / (Vmax - Vref);
    line2.b = (pwRef * (1 + level)) - (Vref * line2.m);
}
```

## Compute Stim From Lines
**PW = insole value * line.m + line.b**
insole value = pressure value aka voltage
```
    if (voltage <= Vth)
    {
        return 0;
    }

    // volage greater than vmax
    if (voltage > Vmax)
    {
        return pwMax;
    }

    if (voltage < Vref)
    {
        return line1.m * voltage + line1.b;
    } else
    {
        return line2.m * voltage + line2.b;
    }
```


Stim set with calculated PW (if it's less than pwMax) and PA value that was programmed in (PA not changeable via the app only by programming the board)

Stim actually *delivered* as an event schedule in AscuAmputee.ino using computed PW 

# Raw Insole Values
```
    // heel: averages two heel pads (sensors 6 and 7)
    pressureValuesDigital[1] = (digitalValues[ADC_CH_LHEEL] * heelWeight) 
                             + (digitalValues[ADC_CH_RHEEL] * heelWeight);

    // midfoot: uses arch (sensor 2)
    pressureValuesDigital[2] = digitalValues[ADC_CH_ARCH];

    // toes: averages toes (sensor 3) and met1 (sensor 5)
    pressureValuesDigital[3] = ((digitalValues[ADC_CH_TOES] * toeWeights[0])
                             + (digitalValues[ADC_CH_MET1] * toeWeights[1])
                             + (digitalValues[ADC_CH_MET3] * toeWeights[2])
                             + (digitalValues[ADC_CH_MET5] * toeWeights[3])
                             + (digitalValues[ADC_CH_HALX] * toeWeights[4])) / 
                             (toeWeights[0] + toeWeights[1] + toeWeights[2] + toeWeights[3] + toeWeights[4])
```



