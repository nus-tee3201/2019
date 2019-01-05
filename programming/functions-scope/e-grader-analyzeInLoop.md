#### Exercise : Grader - Analyze Grades in a Loop

Write a program to analyze grades of multiple students. The grade analysis can be similar to <trigger trigger="click" for="modal:analyzeGradesInLoop-gradeAnalyzer">a grade analyzer you wrote in a previous exercise</trigger> but the program needs to repeat the process until the user chooses to stop.
```python
Enter project score: 10
Enter exam score: 50
Total: 60
Project : ==
Exam    : ==========
Total   : ============
Grade   : B
Continue y/n? y
Enter project score: 50
Enter exam score: 49
Total: 99
Project : ==========
Exam    : =========
Total   : ===================
Grade   : A
Continue y/n? n
```
You are ==required to divide your code into multiple functions==.

<modal large title="" id="modal:analyzeGradesInLoop-gradeAnalyzer">
  <include src="../if/e-grades.md"/>
</modal>