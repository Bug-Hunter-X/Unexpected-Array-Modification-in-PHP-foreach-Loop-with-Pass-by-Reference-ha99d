# PHP Foreach Loop Pass-by-Reference Bug

This repository demonstrates a common, yet subtle, bug in PHP related to the use of pass-by-reference in `foreach` loops.  Improper handling of pass-by-reference can lead to unintended modification of the original array.

The `bug.php` file contains the erroneous code, while `bugSolution.php` provides the corrected version.

## Bug Description

In PHP, the `foreach` loop, when used with `&` (pass-by-reference), modifies the original array directly. If you're not careful about this, you might get unexpected changes to your data.

## Solution

The solution involves avoiding pass-by-reference in the foreach loop if you only need to read the value.  If modification is required, make sure it's intended and handle any side effects appropriately.