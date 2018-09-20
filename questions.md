Question
---
Q1: Why we must handle all exceptions and recover from the failures?

Q2: What are disadvantages of duplication code?

Q3: TDD(Test Driven Development) asks us to write unit tests that cover virtually all of our production code. There are three laws of TDD. Choose three choices that are the laws of TDD.<br>
- [ ] You may not write unit test until you have written a production code.
- [ ] You may not write production code until you have written a failing unit test.
- [ ] You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
- [ ] You may not write more production code than is sufficient to pass the currently failing test.
- [ ] You may write more production code than is sufficient to make sure that all of bugs are already fixed.

Q4: Quite a few problems were fixed in review process. Code reviews are not just for code written by junior developers—you should perform code reviews on the code written by every developer in the team. What should you look for during a code review?

Answer
---
Q1: Perhaps you’re calling some code that might throw an exception; in your own code you can try to handle and recover from that failure. It’s great if you can recover and continue with the processing without your user being aware of any problem. If you can’t recover, it’s great to let the user of your code know exactly what went wrong.

Ref: [PAD](https://github.com/mart0/Useful-materials---books-presentations-ant-etc./raw/master/Others/Practices%20of%20an%20Agile%20Developer.pdf) "Report All Exceptions" (page 139)

Q2:<br>
1.) It represents a missed opportunity for abstraction.<br>
2.) It could probably become a subroutine or perhaps another class outright.<br> 
3.) It makes coding becomes slower and more error.<br>

Ref: [Clean Code](http://www.investigatii.md/uploads/resurse/Clean_Code.pdf) General - G5: duplication (page 289)

Q3:
- [ ] You may not write unit test until you have written a production code.
- [X] You may not write production code until you have written a failing unit test.
- [X] You may not write more of a unit test than is sufficient to fail, and not compiling is failing.
- [X] You may not write more production code than is sufficient to pass the currently failing test.
- [ ] You may write more production code than is sufficient to make sure that all of bugs are already fixed.

Ref: [Clean Code](http://www.investigatii.md/uploads/resurse/Clean_Code.pdf) "Unit Tests" (page 121)

Q4: You might develop your own list of specific issues to check or There’s a very minimal list to get you started:
- Can you read and understand the code?
- Are there any obvious errors?
- Will the code have any undesirable effect on other parts of the application?
- Is there any duplication of code (within this section of code itself or with other parts of the system)?
- Are there any reasonable improvements or refactorings that can improve it?

Ref: [PAD](https://github.com/mart0/Useful-materials---books-presentations-ant-etc./raw/master/Others/Practices%20of%20an%20Agile%20Developer.pdf) "Review Code" (page 165)