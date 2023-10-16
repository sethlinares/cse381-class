# Algorithm Description Document

Author: Seth Linares

Date: 10/7/23 

## 1. Name

Quick Sort

## 2. Abstract
Quick Sort is an efficient, in-place sorting algorithm that sorts a list by breaking it into smaller sublists, then sorting them recursively.


## 3. Methodology
Quick Sort works by selecting a pivot element from the list and partitioning the other elements into two sublists, based on whether they are less than or greater than the pivot. The sublists are then sorted recursively. This process continues until the base case is reached, which is a list of size 0 or 1, which are considered to be sorted by definition. The major advantage of Quick Sort is that it is an in-place sorting algorithm, meaning it does not require any extra storage space. While in the worst case, a bad pivot selection could result in an inefficient runtime, the average case is the same as Merge Sort while using less space.


## 4. Pseudocode

```
PARTITION(data, first, last)
    set pivot index = random integer from first to last
    swap data[pivot index] and data[last]
    set LMGP = first

    for i from first to last - 1:
        if data[i] < data[last]:
            swap data[i] and data[LMGP]
            increment LMGP
    swap data[LMGP] and data[last]
    return LMGP

SORT(data, first, last)
    if first >= last:
        return

    else:
        set pivot = PARTITION(data, first, last)
        SORT(data, first, pivot - 1)
        SORT(data, pivot + 1, last)

```

## 5. Inputs & Outputs

List only inputs and outputs for the SORT function.

Inputs:
* data - list of values that are comparable with each other
* first - the index of the first element in the list
* last - the index of the last element in the list

Outputs:
* data - the same list of values, but sorted

## 6. Analysis Results

* Worst Case: $O(n^2)$

* Best Case: $\Omega(n*log(n))$

