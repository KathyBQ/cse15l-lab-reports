use vim to edit the files

change [index1] to [index2] in [ListExamples.java]
  - use <vim <path>> to show the vim screen of the given path's file.
  - use <H>, <L>, <J>, <K> to turn left, turn right, jump down, jump up through the file, or use the arrow keys to cross the file, then find out the content you want to edit.
    (the effientest way to locating the desired word is to: press </index1>, <enter>. the cursor will locate at the first <index1>. then continuously press <n> to get through all teh <index1>. you can find out your desired one later. 
  - press <i> for doing insertion to be able to edit something.
  - press <enter - the space button> to give a space after that letter. then press <delete> to delete the previous letter that you want to delete. then enter your desired letter/number.
  - after editing, press <esc>, then <shift>, then <;>, then <wq>, <enter> to save and exit the vim file.

--------------------
requirement: reproduce the task from above on your own. for each numbered step starting rigth after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. 

for special characters like <enter> or <tab>, write them in angle brackets with code formating. 

then, summarize the commands you ran and what the effect of those keypresses were.


Steps are as following:

step4: log into ieng6. 
<img width="681" alt="Screen Shot 2023-12-03 at 7 51 33 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/bf62146f-5905-40af-b03b-6d3390e408f0">
<img width="675" alt="Screen Shot 2023-12-03 at 7 51 53 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/337d1a92-f0d8-40b5-b008-20b86ed185ad">

step5: Clone my fork of the repository from my github account.
<img width="713" alt="Screen Shot 2023-12-03 at 8 01 34 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/e8f51df0-f9c1-42a9-abc8-8c2984a8e324">

step6:
I ran the test, and it shows there exists one failure and runs 2 tests. There's the problem on the testMerge2() method. 
I had a test.sh script file. I typed ```<vim> <test.sh>``` to open the vim edit screen of test.sh file. Then press <i> to be into the isertion mode. Then I copied the junit running commands for MAC from the instruction website, and pasted into the the test.sh. See below.
<img width="975" alt="Screen Shot 2023-12-03 at 8 05 05 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/570cf7a8-da18-4080-b998-b52c4688b6e6">
See symbol below:
<img width="726" alt="Screen Shot 2023-11-19 at 10 30 39 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/84ac35f9-f06a-416a-bf69-1054d89dbf83">

step7:
I typed ```<vim ListExamples.java>``` to open the vim editing screen of the ListExamples.java file.
<img width="731" alt="Screen Shot 2023-11-19 at 10 35 25 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/e54b09a2-c5c3-437e-9671-5939dc62505f">

I typed ```/index1 <enter>```, then the cursors will locate at the first ```index1``` variable. I pressed ```<n><n><n><n><n><n><n><n><n>``` to locate the exact location of the needed changed ```index1``` in ```merge()``` method. 
<img width="666" alt="Screen Shot 2023-11-19 at 10 39 58 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/2866dd5c-0603-4159-88eb-fe07439e42bd">

I pressed ```<e>``` to locate the cursor to the end of this word ```index1```. Now the cursor is locating at 1. I pressed ```<L><i><delete><2>```. That means I moved the cursor to one right, start the insertion mode to edit, delete the 1 of index1, and finally insert 2 on the previous 1 position. Changed the index1 to index2. 
<img width="666" alt="Screen Shot 2023-11-19 at 10 46 44 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/4c7f7966-2f16-4b17-8eb5-988f54e9239c">

I pressed ```<esc><shift><;><w><q>```. that means I exit the insertion mode, then save the change and exit the vim screen. I am back to the terminal now. 
<img width="666" alt="Screen Shot 2023-11-19 at 11 08 33 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/398bb64f-6daa-45a9-8b2c-d9a065711b13">

step8:
After changing the ListExamples.java using vim, I typed ```bash test.sh``` to compile and run the tests. It shows they are succeed now. 
<img width="666" alt="Screen Shot 2023-11-19 at 11 08 59 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/96145ae5-dd17-4749-a18b-849769077e08">

step9:
I typed ```git status``` to show my current status. And found I have one modified file needed to be added. I typed ```git add ListExamples.java``` to add this changed file to the git. I typed ```git commit -m "fixed error"``` to give a commit with updated info to the git. Then I entered ```git push``` to push this to my github, and finally entered my github username and password to have access. 
<img width="666" alt="Screen Shot 2023-11-19 at 11 16 40 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/4dd93bb8-cf2f-42de-9e50-afc346fde791">
<img width="584" alt="Screen Shot 2023-11-19 at 11 17 01 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/01f7476b-27e8-4bbd-9299-5accd7be91ba">
<img width="549" alt="Screen Shot 2023-11-19 at 11 17 22 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/fbaeb405-01e3-4413-886e-b76a9a9bfc89">
<img width="558" alt="Screen Shot 2023-11-19 at 11 17 42 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/de9651eb-cfb2-4a4e-b1bb-53787c74b41e">
<img width="558" alt="Screen Shot 2023-11-19 at 11 17 59 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/3aa0afa9-15e2-46d4-85b0-25db1cf02840">
