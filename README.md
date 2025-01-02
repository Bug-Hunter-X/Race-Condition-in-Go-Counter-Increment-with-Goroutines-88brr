# Race Condition in Go Counter Increment with Goroutines

This repository demonstrates a common race condition in Go when using goroutines to increment a shared counter without proper synchronization.  The `bug.go` file contains the buggy code, while `bugSolution.go` provides a corrected version.

## Bug Description

The program launches 1000 goroutines, each incrementing a shared counter.  Without proper synchronization mechanisms, the final counter value might be less than 1000 due to race conditions where multiple goroutines try to update the counter simultaneously.

## Solution

The solution uses a mutex to protect the counter from concurrent access, ensuring accurate increment operations.