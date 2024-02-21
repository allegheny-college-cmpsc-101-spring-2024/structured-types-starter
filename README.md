
# Source Code Survey: Structured Types

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
![Platforms: Linux, MacOS, Windows](https://img.shields.io/badge/Platform-Linux%20%7C%20MacOS%20%7C%20Windows-blue.svg)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Code Style: Black](https://img.shields.io/badge/Code%20Style-Black-blue.svg)](https://github.com/psf/black)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/872320492936257537?logo=discord)](https://discord.gg/kjah8MFYbR)

## Introduction

- Due date: Check Discord or the
  [Course Materials Schedule](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials/blob/main/Schedule.md)
- This assignment is pass/fail. 100%(0%) is earned for a gatorgrade score of 100%(<100%) as
  described in the syllabus section for
  [Assignment Evaluation](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials?tab=readme-ov-file#assignment-evaluation)
- Submit this assignment on GitHub following the expectations in the syllabus on
  [Assignment Submission](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials#assignment-submission).
- To begin, read this `README` based on the Proactive Programmers' project
  [instructions](https://proactiveprogrammers.com/data-abstraction/source-code-surveys/structured-types/)
- This project has been adapted from Proactive Programmers' material, thus discrepancies are possible.
- Post to the #data-structures Discord channel for questions and clarifications.
- For reference, check the
  [starter repo](https://github.com/allegheny-college-cmpsc-101-spring-2024/structured-types-starter)

## Learning Objectives

This assignment is about exploring structured types.
The learning objectives of this assignment are to:

1. Use Git and GitHub to manage source code file changes.
2. Practice using and writing code involving tuples, lists, and higher-order
  functions.
3. Write clearly about the programming concepts in this assignment.

## Seeking Assistance

Please review the course expectations on the syllabus about
[Seeking Assistance](https://github.com/allegheny-college-cmpsc-101-spring-2024/course-materials#seeking-assistance).
Students are reminded to uphold the Honor Code. Cloning the assignment repository is a
commitment to the latter.

For this assignment, you may use class materials, textbooks, notes, and the
internet. Ensure that your writing is original and based on your own understanding
of the concepts. Examples of plagiarism include:

- verbatim copying without citation
- copying with single word modifications
- paraphrasing sections or notes from a source without citation

To claim that work is your own, it is essential to craft the logic and the
writing together without copying or using the logical structure of another
source. The honor code holds everyone to this standard.

If outside of lab you have questions, the #data-structures Discord channel,
TL office hours, instructor office hours, and GitHub Issues can be utilized.

## Project Overview

After cloning this repository to your computer, please take the following
steps:

- Use the `cd` command to change into the directory for this repository.
- Change into the program source code directory by typing `cd source`.
- Run both of the provided Python scripts by typing the following:
  - `python compute-tuple-intersection.py`: demonstrate computation of tuple intersection
  - `python perform-apply-to-each.py`: demonstrate the use of a higher-order function
- Confirm that the programs are producing the expected output.
- Make sure that you can explain why the programs produce the output that they do.
- Run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers from the provided
  source code and `writing/reflection.md`.

## Full Instructions from Proactive Programmers

This assignment invites you to run and observe two Python programs called
`compute-tuple-intersection` and `perform-apply-to-each`. Instead of using the
[Poetry](https://python-poetry.org/) tool for managing dependencies and
packaging these programs, these programs are scripts, without any dependencies
on other Python
packages, that you can run through the Python 3 interpreter. As you continue to
practice a different way to run a Python program, this project offers you the
opportunity to improve your understanding of how to compute the intersection (or
elements in common) between two tuples that can contain an arbitrary number of
values each of an arbitrary type. You will also learn more about high-order
functions as you implement a program that can apply an arbitrary function to the
contents of an arbitrary length list of `int` values.

## Code Survey

If you change into the `source/` directory of your GitHub repository, you will
see two Python files called `compute-tuple-intersection.py` and
`perform-apply-to-each.py`. You can run the `compute-tuple-intersection.py`
program by typing `python compute-tuple-intersection.py` in your terminal
window. This program currently has several `TODO` markers asking you to add
source code from the text book to provide an implementation of a function with
the following signature: `def compute_intersection(tuple_one: Tuple[Any, ...],
tuple_two: Tuple[Any, ...]) -> Tuple[Any, ...]`. Once you have added the
required source code your program should produce the following output. Can you
explain why different calls to `compute_intersection` yield output with the
same elements but in a different order?

```
The first tuple: (1, 'a', 2)
The second tuple: ('b', 2, 'a')

The first intersection tuple: ('a', 2)
The second intersection tuple: (2, 'a')
```

The second program in the `source/` directory is called `perform-apply-to-each`.
Again, this program has several `TODO` markers that invite you to add source
code from the text book to finish the implementation of the function with the
signature `def apply_to_each(values: List[int], function: Callable) -> None`.
After you have added the required source code your program should produce the
following output. One interesting aspect of the `apply_to_each` function is that
it does not return any values, as indicated by the return type annotation of
`None`. If the function does not return a value, then how can it modify the
`values` input parameter of type `List[int]` as shown in the output? Finally,
you will note that `apply_to_each` accepts a `function` parameter of type
`Callable`, making it a higher-order function. What are the benefits of using
high-order functions in Python programs? How does `apply_to_each` use the
`function` parameter?

```
Values before transformations: [1, -2, 3.33]
Values after applying abs: [1, 2, 3.33]
Values after applying int: [1, 2, 3]
Values after applying squaring: [1, 4, 9]
```

## Running Checks

Since this project does not use [Poetry](https://python-poetry.org/) to manage
project dependencies and virtual environments, it does not support the use of
commands like `poetry run task test`. However, you can leverage the relevant
instructions in the [technical
skills](/proactive-skills/introduction-proactive-skills/) to run the command
`gatorgrade --config config/gatorgrade.yml` to check your work. If your work
meets the baseline requirements and adheres to the best practices that proactive
programmers adopt you will see that all the checks pass when you run
`gatorgrade`. You can study the `config/gatorgrade.yml` file in your repository
to learn how
[GatorGrade](https://github.com/GatorEducator/gatorgrade) runs
[GatorGrader](https://github.com/GatorEducator/gatorgrader) to automatically
check your program and technical writing.

## Project Reflection

Once you have finished all of the previous technical tasks, you can use a text
editor to answer all of the questions in the `writing/reflection.md` file. Since
this is a source code survey, you should provide output from running each of the
provided Python programs on your own laptop and then explain how the program's
source code produced that output. A specific goal for this project is to ensure
that you can explain each component of a function's type signature, including
details about its inputs and outputs.

## Project Assessment

Since this project is source code survey, it is aligned with the **remembering**
and **understanding** levels of [Bloom's
taxonomy]. You can learn more about how a
proactive programming expert will assess your work by examining the [assessment
strategy]. From the start to the end
of this project you may make an unlimited number of reattempts at submitting
source code and technical writing that meet the project's specification.
