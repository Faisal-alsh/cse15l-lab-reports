### Lab Report 5

# Grade Script
# Faisal alshinaifi


### Overview

This week’s lab report focuses how to make a grader:

Grade.sh
---
```bash
# Create your grading script here
rm -rf student-submission
git clone --quiet $1 student-submission
cp TestListExamples.java student-submission
cd student-submission

# check if the ListExamples.java file matches the given specifications
if [ -e ListExamples.java ]
then
    echo "File was found"
else
    echo "The ListExamples.java file was not found"
    exit 1
fi

if ! [[ $? -eq 0 ]]
then
   echo "There is a compiler error."
   exit
else
   echo "Correctly compiled"
fi

java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > result.txt

echo "TestListExamples ran"
cat result.txt

failure=$(grep -i "Failures:" result.txt)
tests=$(head -n 2 result.txt | tail -n 1 | grep -o "\." | wc -l)


if [[ $failure == "" ]]
then
  echo "All tests passed. Good Job."
else
  echo "Failed tests:" 
  echo $failure
fi

```

---

  - When running  Gradeserver.java it uses the grade.sh script to grade the ListExampels.

     Here are some examples of using the grader that we built on week 7



 
 ## Example 1: 
 <img width="1470" alt="lab3" src="https://user-images.githubusercontent.com/51794365/204236860-f4dd35d9-0e7f-4ce7-bf87-e1e6206dec0b.png">
 
    - Repository: https://github.com/ucsd-cse15l-f22/list-methods-filename
    - Grade: 0/3
    

 ## Example 2: 
 
 <img width="1470" alt="compileError" src="https://user-images.githubusercontent.com/51794365/204242142-470846d1-cd36-473b-9f55-32f5bdd47563.png">


    - Repository:  https://github.com/ucsd-cse15l-f22/list-methods-compile-error
    - Grade: N/A - Compiler error
   
   
 ## Example 3: 
 
 <img width="1470" alt="perfect" src="https://user-images.githubusercontent.com/51794365/204242923-0f4178aa-ff56-4df0-b6e6-4a8d5254231b.png">

    - Repository: https://github.com/ucsd-cse15l-f22/list-methods-compile-error](https://github.com/ucsd-cse15l-f22/list-methods-corrected
    - Grade: 3/3
    
    
