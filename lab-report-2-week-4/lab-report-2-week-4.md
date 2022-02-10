# Lab Report 2
## Commit 1
![https://github.com/erichu100/markdown-parse/commit/7ef3d2eb634b63b80fb7509d0e747a4c98a0e2e1](noLinkCommit.PNG)
[No link test file.](https://github.com/erichu100/markdown-parse/blob/main/noLinkFile.md)

Output: `IndexOutOfBoundsException.`

![No link symptom.](noLinkSymptom.PNG)

The bug was not checking if open and closed brackets and parentheses were found. As such, when given an input without any parentheses or brackets, the program attempts to run substring with -1 as a parameter (on current build -2 due to image and backslash checks), throwing an IOOB exception.
## Commit 2
![https://github.com/erichu100/markdown-parse/commit/4e7fd095226a500a7fa500760224894f2a93cd5c](fakeLinkCommit.PNG)
[Detached brackets and parenthesis test file.](https://github.com/erichu100/markdown-parse/blob/main/fakeLink.md)

Output: `["(also known as felis catus)"]`

![Fake link symptom.](fakeLinkSymptom.PNG)

The bug was assuming every pair of brackets followed by a pair of parentheses is a link, regardless of distance between the brackets and parentheses. When given an input with text (meow meow meow) between brackets and parentheses, it still returns the text within the parentheses as a link.
## Commit 3
![https://github.com/erichu100/markdown-parse/commit/3d14226d104cfe03d8ee36df3445bd72ba269e46](imageCommit.PNG)
[Image test file.](https://github.com/erichu100/markdown-parse/blob/main/imageTest.md)

Output: `["(https://something.com)", "(some-page.html)"]`

![Image symptom.](imageSymptom.PNG)

The bug was once again assuming every pair of brackets followed by a pair of parentheses is a link, this time not accounting for images. When given an input of two images, it would incorrectly classify the addresses of the images as links.