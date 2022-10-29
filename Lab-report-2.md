### Lab Report 2
# Extend  Server

# Faisal Alshinaifi

### Table of content:

  - [Part 1: Search Engine](#Part-1:-Search-Engine)
  - [Part 2: Fixing Bugs](#Part-2:-Fixing-Bugs)
---
# Part 1: Search Engine

<img width="911" alt="Screen Shot 2022-10-14 at 8 09 36 PM" src="https://user-images.githubusercontent.com/51794365/195966375-a2d7cf75-9023-42e1-aab8-d58d41b724d1.png">


**As seen in the photo below the highlited code is resposible for adding.**


<img width="725" alt="Screen Shot 2022-10-14 at 8 15 02 PM" src="https://user-images.githubusercontent.com/51794365/195966604-9e4bd04d-39f7-4de7-83d6-07492e5829c2.png">

---

**However, searching is diffrent**

<img width="1470" alt="Screen Shot 2022-10-14 at 8 12 47 PM" src="https://user-images.githubusercontent.com/51794365/195966400-53d9151a-82f1-47e1-ba1e-72d1d34be5d9.png">

And this is the Code responsiple for searching a query:

<img width="1470" alt="Screen Shot 2022-10-14 at 8 18 25 PM" src="https://user-images.githubusercontent.com/51794365/195966581-8476ab11-83c8-4a1b-b38c-8799fa5cf6f5.png">



---

# Part 2: Fixing Bugs

## Array reversed bug

As Shown in the picture below  the testReversedTEST1 is failing, and is saying the the first index in theArray is 0 instead of 8.

<img width="1470" alt="Screen Shot 2022-10-28 at 4 41 03 PM" src="https://user-images.githubusercontent.com/51794365/198752966-53f0e8b9-d826-4a6a-bf34-71498c2c89bb.png">


So I went to the method of Reversed To diagnose the problem. When Tracking the code I noticed that issue was with the coping part, The NewAraay is Empty!LOOK AT Line 17!

<img width="1470" alt="Screen Shot 2022-10-28 at 4 49 43 PM" src="https://user-images.githubusercontent.com/51794365/198753135-27527cd1-cc4b-487f-a722-5a1d69b61de1.png">

So to Fix the error I had to fill the newArray with the orignal array's values, and then reverse copy it to the old array.

<img width="1470" alt="Screen Shot 2022-10-28 at 4 57 40 PM" src="https://user-images.githubusercontent.com/51794365/198753247-8c690afb-12a8-48b7-bb9e-dc31113f04b2.png">

## List Merge Bug

 As seen in the terminal the Testing of Merge on line 21 is not working.
 
<img width="1470" alt="Screen Shot 2022-10-28 at 3 49 13 PM" src="https://user-images.githubusercontent.com/51794365/198753506-5ad49223-1816-4506-8308-c8eed7a0e64d.png">

After inspecting the merge method in the ListExamples, I recognized that one of the loops would not end. The while loop in question is at line 41, The condition for the loop to end is if index2 is equal or grater than size. However, the index2 is not incrementing, insted index1 for some reason is increamting inside the loop. hmmmm somthing does not smell right... 

<img width="1470" alt="Screen Shot 2022-10-28 at 5 48 00 PM" src="https://user-images.githubusercontent.com/51794365/198754235-02301d6e-4f30-449f-8266-3b69483b6c0e.png">

So to fix it I just replaced "index1" with "index2".  And now the Test works YAY!

<img width="1470" alt="Screen Shot 2022-10-28 at 5 50 22 PM" src="https://user-images.githubusercontent.com/51794365/198754316-862f5422-9871-4d04-b65f-3deefece043c.png">




