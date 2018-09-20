Question
---
Q1: Why we must handle all exceptions and recover from the failures?

Q2: What are disadvantages of duplication code?

Answer
---
Q1: Perhaps you’re calling some code that might throw an exception; in your own code you can try to handle and recover from that failure. It’s great if you can recover and continue with the processing without your user being aware of any problem. If you can’t recover, it’s great to let the user of your code know exactly what went wrong.

Ref: [PAD](https://github.com/mart0/Useful-materials---books-presentations-ant-etc./raw/master/Others/Practices%20of%20an%20Agile%20Developer.pdf) "Report All Exceptions" (page 139)

Q2:<br>
1.) It represents a missed opportunity for abstraction.<br>
2.) It could probably become a subroutine or perhaps another class outright.<br> 
3.) It makes coding becomes slower and more error.<br>

Ref: [Clean Code](http://www.investigatii.md/uploads/resurse/Clean_Code.pdf) General - G5: duplication (page 289)
