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


if [[ $failure == "" ]]
then
  echo "All tests passed. Good Job."
else
  echo "Failed tests:" 
  echo $failure
fi

```

---


# Testing

  - When running  Gradeserver.java it uses the grade.sh script to grade the ListExampels.

     Here are some examples of using the grader that we built on week 7



 
 - Example 1 
 <img width="1470" alt="lab3" src="https://user-images.githubusercontent.com/51794365/204236860-f4dd35d9-0e7f-4ce7-bf87-e1e6206dec0b.png">
 
    - Repository: https://github.com/ucsd-cse15l-f22/list-methods-filename
    - Grade: 0/3
    

 - Example 2  
 
 <img width="1470" alt="compileError" src="https://user-images.githubusercontent.com/51794365/204242142-470846d1-cd36-473b-9f55-32f5bdd47563.png">


    - Repository:  https://github.com/ucsd-cse15l-f22/list-methods-compile-error
    - Grade: N/A - Compiler error
   
   
 - Example 3  
 
 <img width="1470" alt="perfect" src="https://user-images.githubusercontent.com/51794365/204242923-0f4178aa-ff56-4df0-b6e6-4a8d5254231b.png">

    - Repository: https://github.com/ucsd-cse15l-f22/list-methods-corrected
    - Grade: 3/3
    
    
# Trace the Script

## I will trace example 2 : Compile Error

```
# Create your grading script here
rm -rf student-submission
git clone --quiet $1 student-submission
cp TestListExamples.java student-submission
cd student-submission
 
```
   - First   `rm -rf student-submission` removes any directory called `student-submission` so it becomes available.
   - The `git clone --quiet $1 student-submission` clones the student-submission directory but supresses the output.
   - Neither an standard error nor an standard output is produced.
   - Exits with code `0 ` because the directory exsists.
  
  
## Now for the testing of the file:

```
if [ -e ListExamples.java ]
then
    echo "File was found"
else 
    echo "The ListExamples.java file was not found"  // (will NOT run)
    exit 1  // (will NOT run)
fi
```

- The if statment Checks if the file exists by using `-e` 
- `echo "File was found"`  basicly means print "File was found"
-  No output/error will be produced thus exit code `0` 

```
if ! [[ $? -eq 0 ]]
then
   echo "There is a compiler error."
   exit 
else  // (will NOT run)
   echo "Correctly compiled" // (will NOT run)
fi  // (will NOT run)

```
 - the if statment checks if the file `ListExamples.java` does not compiles (psstt.. it does not)
 -  Then the then statment is occurs.
 -  `echo "There is a compiler error."` prints "There is a compiler error."
 -  Finally the code exits
 -   The program finishes by exiting with a `0` code.

```
java -cp .:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples > result.txt // (will NOT run)

echo "TestListExamples ran" // (will NOT run)
cat result.txt // (will NOT run)

failure=$(grep -i "Failures:" result.txt) // (will NOT run)


if [[ $failure == "" ]] // (will NOT run)
then // (will NOT run)
  echo "All tests passed. Good Job." // (will NOT run)
else // (will NOT run)
  echo "Failed tests:"  // (will NOT run)
  echo $failure // (will NOT run)
fi // (will NOT run)

```
- These lines Do NOT run since the file did not compile then Exited.



## THANK YOU!!



