# Rust Borrow Checker Error: Immutable Borrow After Mutable Borrow

This repository demonstrates a common error in Rust related to borrowing and mutability. The example code attempts to create an immutable reference to a vector element, then modifies the vector. This violates the borrow checker's rules and leads to undefined behavior.  The solution showcases how to correctly handle mutability and borrowing to avoid this issue.

## Bug Description

The `bug.rs` file contains code that attempts to print the value of an element in a vector after the vector has been modified (pushing a new element).  This creates an immutable borrow of the vector element, followed by a mutable borrow (through the push operation), violating the borrow checker's rules, resulting in a compile-time error or runtime panic.

## Solution

The `bugSolution.rs` file provides a corrected version of the code.  This version avoids the error by either creating a copy of the element of interest before modifying the vector or restructuring the code to eliminate the concurrent immutable and mutable borrow.  The readme further details the approach.