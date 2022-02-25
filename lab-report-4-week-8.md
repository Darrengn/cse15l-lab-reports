[Back](https://darrengn.github.io/cse15l-lab-reports/index.html)

# Lab Report 4

[My Repo](https://github.com/Darrengn/markdown-parse)  
[Reviewed Repo](https://github.com/artballesteros/markdown-parse)

## Snippet 1

Expected output: [`google.com]

Test: ![Image](/LabFourPics/Pic1.png)

My Output: ![Image](/LabFourPics/Pic2.png)

Reviewed Output: ![Image](/LabFourPics/Pic3.png)

Code change: I think that I could make a simple code change where I find the index of the first "\`" and check if it is between the index of the "[" and the "]". If it is, then you set current index to the index of the "\`" and continue.

## Snippet 2

Expected output: [a.com, a.com(()), example.com]

Test: ![Image](/LabFourPics/Pic4.png)

My Output: ![Image](/LabFourPics/Pic5.png)

Reviewed Output: ![Image](/LabFourPics/Pic6.png)

Code change: I think that this would be a longer fix. The issue in my code is that it can not differentiate from different ammounts of ")". In order to fix this, I think that I would need to count parenthesis and make sure that there are matching number of open and close parenthesis. 

## Snippet 3

Expected output: [https://ucsd-cse15l-w22.github.io/]

Test: ![Image](/LabFourPics/Pic7.png)

My Output: ![Image](/LabFourPics/Pic8.png)

Reviewed Output: ![Image](/LabFourPics/Pic9.png)

Code change: To fix this, I would need to get the index of the new line character and chack to see if it is between the "[" "]" or the "(" ")". If it is, then you skip to the next "]" or ")" and then set that value to the closing parenthisis or bracket and continue.