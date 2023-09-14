---
Priority: Completed
Area: GirlsWhoCode
Status: Done
---
[https://docs.google.com/document/d/1zD555qNJvnodHfjuiEC175ukqIhzxGvl3bV0SkP-JxI/edit](https://docs.google.com/document/d/1zD555qNJvnodHfjuiEC175ukqIhzxGvl3bV0SkP-JxI/edit)

  

[https://docs.google.com/presentation/d/12HznQ8vqHLmayy1EWK3pr7jccZcHoUQ89ypWWc_vdqQ/edit#slide=id.gf56f5bba93_0_657](https://docs.google.com/presentation/d/12HznQ8vqHLmayy1EWK3pr7jccZcHoUQ89ypWWc_vdqQ/edit#slide=id.gf56f5bba93_0_657)

  

To Add

- Circuits General
    - Why series vs //: redundancy, power multiple things
    - Why care about low level: digital features can be done with analog circuitry, more reliable, everything you code will be reading values and setting values of electric signals
- Buttons + LEDs
    - Ground: reference point, current will flow back to this
        - Open and short circuits
    - LED: also feel for the flat side
    - Why do you need the resistor: prevent the LED from drawing a lot of current → burn out
        - Current drop across components ? [https://www.sparkfun.com/tutorials/219](https://www.sparkfun.com/tutorials/219)
    - Reading resistor values?
- Programming
    - Show how many loops / sec
    - Concept of program starting as soon as it’s plugged in

Power point: read and write mode

  
Writing out code flow before coding

  

Group

- IDE 2.0
- State detection in a loop : button press counter
- Documentation : [https://www.arduino.cc/reference/en/](https://www.arduino.cc/reference/en/)
- Writing out

  

  

  

Big ideas

- [https://www.geeksforgeeks.org/difference-between-abstraction-and-encapsulation-in-java-with-examples/](https://www.geeksforgeeks.org/difference-between-abstraction-and-encapsulation-in-java-with-examples/) encapsulation creates abstraction

[http://www.ladyada.net/learn/arduino/lesson5.html](http://www.ladyada.net/learn/arduino/lesson5.html)

  

  

  

# Arduino Teaching Tips

Pull up / pull down: prevent undefined values

- Direct 5V to ground wire has indeterminate voltage based on wire resistance values
- Adding a resistor causes a definite voltage drop across it; known values on both ends
    - Can be on source or ground side
- Allows switching between voltage values i.e. button

Heap Fragmentation

- segments of allocated + empty space
- No continuous space of memory of certain sizes
- Use other memory areas