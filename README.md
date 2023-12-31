# leetcode-python

## Overview

Setup an environment for TDD oriented solutions of leetcode problems using Python3.

## Setup

### Prerequisites

- Python3
- PyTest

*Assumption: Python3 and PyTest are installed globally, so no need for virtual environments.*  

## Initializing a new problem

A new problem folder can be initialized using the `init-problem.py` script.

This script requires the following parameters:

- <problem_number> an integer that corresponds to the leetcode problem number.
- <problem_name> the name of the leetcode method used to invoke the solution

Note that the problem name must contain only letters and numbers. This allows us to emit valid Python modules that include the problem name. Consult leetcode to get the problem name before initializing.

*For example, problem #1, 'Two Sum' has the following method definition:*

`def twoSum(self, input: List[int], target: int) -> List[int]:`

*... and so the problem name is 'twoSum'. When initializing this problem:*

`python3 init-problem.py 1 twoSum`

## Examine the new problem folder
Each problem is set up in a subdirectory under the `algorithms` subfolder.

The `init-problem.py` script does the following:

1. Creates a new subdirectory for the problem
2. Creates a `problem.md` file 
3. Creates a solution file with a sample solution class
4. Creates a tests file with a table-driven test

## Edit the initialized problem before working

1. Navigate to the problem subdirectory.
2. Copy/paste the problem description from leetcode into the `problem.md` file.
3. Edit the test file `test_data` to match the examples from the leetcode problem description.
4. Edit the solution class' method signature to match the example from leetcode
    - *The method signature must match the invocation in the test script!*

## Working a problem locally

1. Navigate to the problem subdirectory.
2. Run `pytest -v` to test the existing solution
3. Edit the solution file to implement/revise the solution function.
4. Repeat #2 and #3 to arrive at a solution that satisfies the examples provided by leetcode.

## Running a problem in leetcode

When the solution passes all the example `test_data` locally, copy the solution class and paste it into leetcode's editor, then click [Run].

Observe that leetcode runs the solution and check to output for errors. Review any errors and revisit the solution locally to correct the method. 

> Note that leetcode will only test your solution against the example `test_data` during [Run].

## Submitting a problem to leetcode

Once you are satisfied that the solution passes tests proposed by the example data, click [Submit]. This submits the solution to the leetcode judge. the judge runs the solution with additional test data to verify the correctness and performance of the solution.

> Note that the leetcode judge will usually impose additional edge cases which must be addressed. If your solution does not handle these cases, simply copy the new unexpected edge case input parameters to a new entries in `test_data` and return to working on the solution.

## Completing a problem

Once you have completed a problem and passed the leetcode judge submission process, review the code folder and then commit to github. This maintains a clean set of solutions and a history of how you approached solving these problems.

Congratulations! Your next step is to choose a new problem and repeat this process. 

My own experience of approaching leetcode this way was centered around a time-boxed (45 minute) period in the early morning. If a problem was not complete at the end of my time-box, I would simply continue the next morning and work the cycle.

## Enjoy

I hope this approach aids you in hacking through leetcode problems, and especially that it elevates your happiness in coding.
