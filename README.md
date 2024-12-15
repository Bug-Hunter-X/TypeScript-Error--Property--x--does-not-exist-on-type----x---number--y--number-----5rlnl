# TypeScript Bug: Optional Property Issue

This repository demonstrates a common TypeScript error related to optional properties and type checking.  The bug arises from an incorrect type definition that leads to a compile-time error when attempting to access a potentially undefined property.

## Bug Description

The `printCoord` function expects an object with `x` and `y` properties. However, the type definition for `pt` incorrectly marks `x` as optional (`x?: number`). When the function attempts to access `pt.x`, TypeScript throws an error because `x` might be undefined.

## Solution

The solution involves correcting the type definition for `pt` to ensure that `x` is always defined. This removes the ambiguity and allows the code to compile without errors.