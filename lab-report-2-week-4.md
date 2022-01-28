[Back](https://darrengn.github.io/cse15l-lab-reports/index.html)

# Lab Report 2

## Code Change 1<br>

### Code Diff 1

![image](/LabTwoPics/Pic1.png)

### [Failure Inducing Input](https://darrengn.github.io/cse15l-lab-reports/test3.html)

### Symptom 1

![image](/LabTwoPics/Pic2.png)

### Relationship

The bug of not checking for a -1 creates a symptom because the "](" string couldn't be found in the file. The symptom appears because of how the substring method works. Because the indexOf method returns -1 when it can't find the specified string, the substring method gets a parameter of -1, which causes it to throw this exception.

## Code Change 2 <br>

### Code Diff 2

![image](/LabTwoPics/Pic3.png)

### [Failure Inducing Input](https://darrengn.github.io/cse15l-lab-reports/test-file6.html)

### Symptom 2

![image](/LabTwoPics/Pic4.png)

### Relationship

The bug is that the program will take the links to images out as well as normal links, and the symptom for this is seeing an output from an image link when we expect an empty output. Because the image and link formmating are similar in markdown, this causes a bug. The issue is fixed by checking for an "![" which differentiates between a image and link.

## Code Change 3 <br>

### Code Diff 3

![image](/LabTwoPics/Pic5.png)

### [Failure Inducing Input](https://darrengn.github.io/cse15l-lab-reports/test-file8.html)

### Symptom 3

![image](/LabTwoPics/Pic6.png)

### Relationship

The bug is that the program will print out a link even if it isn't clickable, which is shown by the symptom of something being printed out even when nothing should be printed. The issue comes from the fact that if the [] are empty in markdown, there is no where to click on to access the link. To check this, you can check if the index of the [ is one less than the index of the ].