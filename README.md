# Turing Machine Emulator

Simple Turing Machine Interpreter. Supports quadruplet rules. According to _Wikipedia_:
> A Turing machine is a mathematical model of computation that defines an abstract machine that manipulates symbols on a strip of tape according to a table of rules. Despite the model's simplicity, given any computer algorithm, a Turing machine capable of simulating that algorithm's logic can be constructed.   

## Demo

This animation illustrates turing machine performing bitwise and operation on two binary operands. Repository contains "bitwise_and" file with rules required to run this algorithm. Machine copies input data and then perfomes logical operation on two operands.


![Alt Text](https://github.com/curlysilk53/turing-machine/blob/master/bitwise_and_demo.gif)


## Usage: 

`turing-machine.sh <file> <tape_data> [options]`
+ `<file>` - file with rules
+ `<tape_data>` - initial tape state
+ `[options]` - valid options




## Options


Available options:  
+ -s <speed_value_s> sets visualization delay (default: 0.1s)
+ --help displays detailed information about using this script


## Rules format

Files with rules should include transitions, each on new line  
Transitions should have followng structure: **[st1,sym,ins,st2]**  

+ st1 - current_state (alphanumeric)  
+ sym - symbol currently seen on a tape
+ ins - instruction or symbol to write
+ st2 - next state  (alphanumeric)  

## Instructions

Instructions are used to control head and finish execution
+ \>  - head should move to the right 
+ \<  - head should move to the left
+ \=  - head should stay at the same place
+ \#  - instruction finishes execution

## Notes

+ Machine tape is left limited  
+ Each command should be stated in a newline  
+ Script detects trivial loops 
+ Script detects indeterminant transitions 
+ You can leave comments in rules using \#
