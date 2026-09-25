# CMPS 2200 Assignment 3
## Answers

**Name:** Chuong Hoang Pham

_________________________


Place all written answers from `assignment-03.md` here for easier grading.


**1: Searching Unsorted Lists**

- **1b.** Work and span of `isearch` implementation

    Work: $O(n)$

    Span: $O(n)$

    Since it does a sequential search through the list.

- **1d.** Work and span of `rsearch` implementation

    Work: $O(n)$

    Span: $O(\log n)$

    Since it does a divide and conquer approach to search the list.

- **1e.** Work and span of `rsearch` using `ureduce`

    Work: $O(n)$

    Span: $O(\log n)$

    Since it splits the list into unbalanced chunks (1/3 and 2/3) recursively, the tree depth is bounded by $\log_{3/2} n$ and total work over all nodes remains $O(n)$.

**3: Parenthesis Matching**

- **3b.** Recurrences and Big-Oh solutions for `parens_match_iterative`

    Work: $O(n)$

    Span: $O(n)$

    Since it iterates through the list sequentially.

- **3d.** Work and Span for `parens_match_scan`

    Work: $O(n)$

    Span: $O(\log n)$

    Since it relies on `scan`, `map`, and `reduce`, which are highly parallelizable operations taking $O(n)$ work and $O(\log n)$ span.

- **3f.** Recurrences and Big-Oh solutions for `parens_match_dc_helper`

    Work: $O(n)$
    
    Span: $O(\log n)$

    Since it divides the list in half recursively and does $O(1)$ work to merge, the recurrences are $W(n) = 2W(n/2) + O(1)$ and $S(n) = S(n/2) + O(1)$.
