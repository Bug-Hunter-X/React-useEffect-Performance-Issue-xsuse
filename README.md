# React useEffect Performance Issue

This repository demonstrates a common performance issue in React applications involving the `useEffect` hook.  The `useEffect` hook, while powerful, can lead to performance problems if not used carefully.  This example shows an inefficient implementation and provides a solution for optimization.

## Problem

The provided code includes a `useEffect` hook that runs after every render, logging the current count to the console. This is inefficient, especially with frequent updates to the `count` state.  Each render triggers the effect, leading to unnecessary re-renders and potential performance degradation.

## Solution

The solution uses the optional second argument of `useEffect` to control when the effect runs. By including `[count]` as the second argument, the effect only runs when the `count` variable changes. This significantly improves performance by avoiding unnecessary re-renders and log outputs.