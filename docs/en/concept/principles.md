# Principles

This document outlines the core principles of how the Central Infrastructure Controller (CIC) operates. These principles are not optional; they are structural truths built into the system’s foundation.

## 1. Actual state ≠ Desired state

The system makes a clear distinction between the *current reality* (what it sees) and the *declared plan* (what is defined). CIC continuously works to reconcile these two.

## 2. All entities are described declaratively

There is no manual configuration or scripting of changes – we define *what should be*, and the system derives the necessary actions.

## 3. Validation comes before everything

Any data, object, or change must be schema-valid before entering the system. Validation is not a feature – it is the integrity boundary.

## 4. No workarounds – only compliant solutions

If something needs to be “handled differently,” the system can’t guarantee correctness. Every entity is either in the graph or out of scope.

## 5. All changes are traceable

The system logs all state changes, enables reversibility, and understands consequences. Nothing happens silently.