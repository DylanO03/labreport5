# Debugging
---
  1) Lab 6 Help
     <p style="font-size:16px;">I am currently having an issue with my grade.sh code in the list-examples-grader repo for lab 6.
     It seems that no matter which student submission I use, the file always fails a single test,
     even though I have way more than just 1 test. The grader can find the ListExamples.java file in
     the given repo just fine, and everything compiles without issue, but then it just says that there
     was a single test that failed. I attached what I see from the terminal and the code block where the
     error must be coming from, but I am at a loss, why does it only say one test, and why is it failing?</p>
     
     ![Code symptom](Symptom2.png) ![Command line symptom](Symptom1.png)
     ---
  2) Something to Think About
     <p style="font-size:16px;">Hello, after looking over your problem, I agree that the issue is in your code in the given picture.
     I will direct you to think about where the issue could be if it's after compiling, and assuming the
     given files work as expected if they were to run. This seems to leave only one area left for an error
     such as this to occur. Perhaps you could try properly executing everything manually from the command
     line? Please follow up if you are still stuck/confused.</p>
     
     ---
  3) Fixed
     ![Code fixed](Fixed2.png) ![Command line fixed](Fixed1.png)
     <p style="font-size:16px;"> The issue was that instead of passing an appropriate test class to java  
     when attempting to run the test file, they were instead passing the class with the ".java" extension,  
     or the name of the file instead of the class. This resulted in a failure to run the right class in  
     JUnit, which is why there was a failure of only one test.
