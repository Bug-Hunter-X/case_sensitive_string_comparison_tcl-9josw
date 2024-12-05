# Case-Sensitive String Comparison Bug in Tcl

This repository demonstrates a common but subtle bug in Tcl related to case-sensitive string comparisons.  The `badproc.tcl` file contains a Tcl procedure that incorrectly handles string comparisons, leading to unexpected results when strings differ only in capitalization.  The corrected version, `badproc_fixed.tcl`, illustrates the proper use of case-insensitive comparisons.

## Bug Description

The original Tcl procedure uses the `==` operator for comparison.  This operator performs a case-sensitive comparison.  If two strings are identical except for case, this leads to an incorrect comparison result.

## Solution

The solution uses the `eql` operator instead of `==`. This operator performs a case-insensitive comparison, thus correctly handling cases where strings differ only in their capitalization.