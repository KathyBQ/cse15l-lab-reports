part 1 - debugging scenario

I went to the grade review test project, ran it with ```bash grade.sh <the test url>``` to compile and run the project. See the symbol below. There's a failure with error of ```incompatible types``` at ```ListExamples.java. I guess the error is the type. 
<img width="925" alt="Screen Shot 2023-12-03 at 11 49 00 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/4babd855-6604-475c-98b2-f1c8256f9bbc">

TA reponse: The arguments have the wrong the order for 2 arguments of ```filter``` method  so that it doesn't match the expected behavior.
<img width="498" alt="Screen Shot 2023-12-04 at 11 34 31 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/1e1bb003-f2c9-4f1a-b44a-6029568fa825">

Answer: change the 2 arguments' order of the ```filter``` method in my github forked repository.
<img width="498" alt="Screen Shot 2023-12-04 at 11 22 04 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/fcb497ec-7a22-4b12-b045-d075d5fe61df">

Then run the grade again to get the pass version. 
<img width="954" alt="Screen Shot 2023-12-04 at 11 19 48 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/e99154b9-a130-4dc2-b40d-3882bc0f2e6f">

<img width="316" alt="Screen Shot 2023-12-04 at 11 37 54 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/4b11c9e6-a8f8-4f30-a225-b5fbc43568a4">

before fixing the file:
<img width="509" alt="Screen Shot 2023-12-04 at 11 38 40 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/24d96bb8-ce5b-4851-8a04-dad6415aef19">

after fixing the file:
<img width="509" alt="Screen Shot 2023-12-04 at 11 39 43 PM" src="https://github.com/KathyBQ/cse15l-lab-reports/assets/96004027/da34b977-bcc6-4b2d-9adf-97134a5f3996">

command line to run the bug: ```bash grade.sh https://github.com/KathyBQ/student-example-1.git```

I swap the order of 2 arguments ```List<String> list``` and ```StringChecker sc``` for  ```filter``` method in ```ListExamples.java``` file. 

part 2 - reflection

I learn a lot and find so many interesting lab experience in this quarter. In these few weeks, I found a lab partner to work together. When I or he had problems or got confused, we conmmunicate each other to talk about our thoughts for labs. I love the ```find``` and ```greb``` commands because they can help me a lot to adderess the desired directories or files in a large project. But I also was sad that all classmates including were so shy. We were hard to connect to each other at the first. 
