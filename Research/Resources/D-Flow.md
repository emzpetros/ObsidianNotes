  

Changes

- DO NOT turn off DFLOW computer
- Turn on audio before opening dflow - HMDI2
    - Will have no DRS window

# To Do

- [x] Work out what controls the Run panel should have
- [x] control flow for randomizing tasks
    - [x] main triggering block
- [x] VStroop
    - [x] background Cube spawning
    - [x] Prevent duplicates
- [x] Astroop
    - [x] wav files [https://voicemaker.in/](https://voicemaker.in/)
    - [x] Check audio actually works
    - [x] Improved wav files (slower voice)
- [x] Improve walk control to work similarly
- [x] Log correct number of responses and subject and which block and what the trial was, time stamp
- [x] Display correct answer
- [x] Instead of start tone separate steps to record data and start treadmill
- [x] Avoid incorrect color at end of trial block
- [x] _Fix naming inconsistencies between trial (30 [task_duration] seconds of a task) and task (differentiates walk, vstroop, astroop), stimulus - occurs at an interval in the 30 seconds_
- [x] Make sure the subject is logged correctly from the run window : manually change file name in Record Data Block
- [x] ~~_Add spacing for print outs (7 lines available at once)_~~
- [x] change opaqueness during walking so you can see the ground
- [x] Implement new alternating stroop task
    - [x] Remove astroop
    - [x] Change walking task to be the same logic as VStroop but display a different message
        - [x] Change the “correct” response
    - [x] Add additional message to vstroop
    - [x] Words centered
    - [x] sensitivity low
    - [x] Add an event E for the end of a task block
    - [x] Shuffle or alternate task order
- [x] Remove redundant set active to 0 in walk trial in main app
- [x] Verify functions
    - [x] Treadmill action: if possible self paced
    - [x] Projector spacing and colors
    - [x] Alternating + random order
    - [x] Correct answer outputs

  

  

  

# DFlow marker lableing

[https://www.protocols.io/view/protocol-3d-gait-analysis-using-treadmill-approach-8epv597zng1b/v1](https://www.protocols.io/view/protocol-3d-gait-analysis-using-treadmill-approach-8epv597zng1b/v1)

# Data Analysis

[https://www.protokinetics.com/measuring-spatiotemporal-parameters-time-stance-phase/](https://www.protokinetics.com/measuring-spatiotemporal-parameters-time-stance-phase/)

[https://www.sciencedirect.com/science/article/pii/S0021929001001749](https://www.sciencedirect.com/science/article/pii/S0021929001001749)

# Code Notes

EventA triggered when tasks start, marked in data

# Editor Notes

1 grid section = 1 m

WalkCognition previous project

Can only pass outputs that are numbers, no bools

  

Need to use HBM if we need labeled markers in DFlow from Vicon

  

300Hz sample

# Lua Notes

Booleans: Lua considers both zero and the empty string as true in conditional tests.

Numbers: `4 0.4 4.57e-3 0.3e12 5e+20`, no ints

Strings: .. = string concatenation

Convert num to String: tostring(#) or E .. “”

Starts counting at 1

Tables

- Size:

```
    print(table.getn{10,2,4})          --> 3    print(table.getn{10,2,nil})        --> 2
```

#### String Escape Codes

|\a|bell|
|---|---|
|`\b`|[[back space]]|
|`\f`|[[form feed]]|
|`\n`|[[newline]]|
|`\r`|[[carriage return]]|
|`\t`|[[horizontal tab]]|
|`\v`|[[vertical tab]]|
|`\\`|[[backslash]]|
|`\"`|[[double quote]]|
|`\'`|[[single quote]]|
|`\[`|[[left square bracket]]|
|`\]`|[[right square bracket]]|

  
  

Tables:

A common mistake for beginners is to confuse `a.x` with `a[x]`. The first form represents `a["x"]`, that is, a table indexed by the string `"x"`. The second form is a table indexed by the value of the variable `x`. See the difference:

```
    a = {}    x = "y"    a[x] = 10                 -- put 10 in field "y"    print(a[x])   --> 10      -- value of field "y"    print(a.x)    --> nil     -- value of field "x" (undefined)    print(a.y)    --> 10      -- value of field "y"
```

Use nil to signal end of array

Because we can index a table with any type, when indexing a table we have the same subtleties that arise in equality. Although we can index a table both with the number `0` and with the string `"0"`, these two values are different (according to equality) and therefore denote different positions in a table. By the same token, the strings `"+1"`, `"01"`, and `"1"` all denote different positions. When in doubt about the actual types of your indices, use an explicit conversion to be sure:

```
    i = 10; j = "10"; k = "+10"    a = {}    a[i] = "one value"    a[j] = "another value"    a[k] = "yet another value"    print(a[j])            --> another value    print(a[k])            --> yet another value    print(a[tonumber(j)])  --> one value    print(a[tonumber(k)])  --> one value
```

  

Logical Operators

The operator **and**  
 returns its first argument if it is false; otherwise, it returns its second argument. The operator **or**  
 returns its first argument if it is not false; otherwise, it returns its second argument: