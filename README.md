# IZLO – Project 1: SAT solver

## Author

- **Name:** Maksim Kalutski
- **Login:** xkalut00

## Introduction

This project involves creating a SAT solver application to help your uncle Pat efficiently plan his postal routes so he
only travels each street once without backtracking. As a postman approaching retirement, Uncle Pat, accompanied by his
cat, seeks a more systematic approach to daily deliveries.

## Assignment

The problem instance consists of a number of intersections (`n`) and a list of `m` streets. Each street is a one-way and
connects two intersections, represented as pairs of numbers denoting the start and end intersections. The task is to
generate a formula whose models are solutions to this problem, creating a path that visits each street exactly once.

## Project structure

- `add_conditions.c`: This file contains functions that need your implementation to generate necessary conditions in CNF
  for the SAT solver:
    1. `at_least_one_valid_street_for_each_step`: Ensure at least one existing street is chosen per step.
    2. `at_most_one_street_for_each_step`: Restrict the choice to one street per step.
    3. `streets_connected`: Ensure that consecutive streets in the path connect properly.
    4. `streets_do_not_repeat`: Prevent any street from being visited more than once.

## Input format

The input format consists of two numbers on the first line indicating the total number of intersections and streets,
followed by the list of streets, each represented by a pair of numbers.

## Testing

You can use the `make test` command to check the basic functionality of your implementation with the sample inputs found
in the `tests/sat` and `tests/unsat` directories.
