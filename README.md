**Code Injection Attacks Detection in Hybrid Applications using CNN**

**Prasanna Sai Puvvada, Singupuram Viswaja, and Dr. Manjubala Bisi**

**Introduction**

**Why this Project?**

- HTML5 hybrid apps have become more and more popular because of their portability on different systems.
- One has found ways to inject malicious code into HTML5 hybrid apps to gain permissions and confidential data as a result mobile security has become more important.

**Problem Statement**

HTML5 hybrid apps are prone to code injection attacks because of mixture of HTML5 and Javascript code

**What is code injection?**

- Data and code can be mixed together
- Attacker can inject a code 

*var password=getPassword()*   
*<script>*

*{access user password  }* 

*</script>";*

- Once it runs, the user password is accessed and user security is lost

**Approach**

![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 004](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/86c06ae7-08c2-4f9d-922a-4e2e56e34a24)

- Detection of code injections

Novel  Deep Learning  Network 
Hybrid Deep Learning Network (HDLN) 

- Code injections are associated with Javascript code  Abstract Syntax Tree (AST) can represent the structure of JavaScript code
- Extract features from AST


**Generation of N-gram features**

![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 005](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/c45abcc5-082a-44eb-8dbd-0b1f97a8f0a3)


AST of Javascript code can be obtained by “Esprima.Parse” in Json format     Example of javascript code

var answer = 6\*7


function test() 
*{*

*alert(“hello world”);*

*}*



**Abstract Syntax Tree**


![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 006](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/1e430f98-24d0-4076-84a4-b3f6ae83f762)



**Generation of N-gram!**


![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 007](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/9b114198-c0d0-4a8e-add7-62a67a94cc00)


**Feature selection**

- Information gain can be used for feature selection

![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 008](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/0591a4f7-3f4c-4302-a3ec-bf828cd88d47)


- Top 800 key features can be used for training the model

  

**Experimental Results**


![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 009](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/52770fe9-b546-4443-a820-51b9c3ff26fe)



![Aspose Words 27d199cc-b147-4352-98d3-390c5adb95d0 010](https://github.com/pprasannasai/Detect_Code_Injection/assets/39426755/d979e20b-4216-4632-a45c-be50e9b1d69c)


**Conclusion**

- Code injection attacks in hybrid applications are detected using a convolutional neural network (CNN). 
- Abstract syntax tree is constructed from JavaScript code of application. Then, Features are extracted from it. 
- Features are selected using information gain and chi square test feature selection technique. 
- The class imbalance problem is tackled by SMOTE data sampling method. 
- CNN is used to train the preprocessed data to predict whether a hybrid application as normal or vulnerable. 
- Experiments are conducted on 85 mobile apps downloaded from Google play store. 
- Classification accuracy of CNN is compared with machine learning models such as NB, Linear SVC and KNN. 
- CNN is able to provide better prediction accuracy for code injection attacks in hybrid applications. Static analysis of hybrid apps are considered in this work.![ref1]
