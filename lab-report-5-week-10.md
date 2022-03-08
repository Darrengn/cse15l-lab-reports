[Back](https://darrengn.github.io/cse15l-lab-reports/index.html)

# Lab Report 5

## Seeing Differences

I used the command `vimdiff test/results.txt markdown-parse/results.txt` to see the difference between the two files. My own code is in the markdown-parse directory and the supplied code is in the test directory

## Diff 1 201.md

Test File: 

![Image](/LabFivePics/Pic2.png)

Outputs: 

![Image](/LabFivePics/Pic1.png)

The expected output is  `[]` because the `]` and the `(` are not next to eachother. Therefore my implementation is correct for this test case.

The bug in the supplied code is that it doesn't check if the `]` is next to the `(`. The fix is as easy as updating checking if the index of the `(` is one greater than the index of `]`. This can be done on line 66 of the code.

![Image](/LabFivePics/Pic3.png)

## Diff 2

Test File: 

![Image](/LabFivePics/Pic4.png)

Outputs: 

![Image](/LabFivePics/Pic5.png)

The expected output is  `[]` because there is a space in the link. Therefore my implementation is incorrect for this test case.

The bug in the supplied code is that it doesn't check if there is ` ` in the link. The fix is easy because all you need to do is check if the substring that is going to be added to the array list contains a ` `, which can be done with `indexOf(" ")`. If the function returns anything besides -1, then you don't add the string to the array list.

![Image](/LabFivePics/Pic6.png)