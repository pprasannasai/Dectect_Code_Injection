**Code Injection Attacks Detection in Hybrid Applications using CNN**

**Prasanna Sai Puvvada, Singupuram Viswaja, and Dr. Manjubala Bisi**

**Introduction**

**Why this Project?**

- HTML5 hybrid apps have become more and more popular because of their portability on different systems.
- One has found ways to inject malicious code into HTML5 hybrid apps to gain permissions and confidential data as a result mobile security has become more important.![ref1]

**Problem Statement**

HTML5 hybrid apps are prone to code injection attacks because of mixture of HTML5 and Javascript code![ref1]

**What is code injection?**

- Data and code can be mixed together
- Attacker can inject a code 

`      `*var password=getPassword()       <script>*

`         `*{access user password  }* 

`       `*</script>";*

- Once it runs, the user password is accessed and user security is lost![ref1]

**Approach**

- Detection of code injections  ![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.004.png)


`            `Novel  Deep Learning  Network 

`           `Hybrid Deep Learning Network (HDLN) 

- Code injections are associated with Javascript code  Abstract Syntax Tree (AST) can represent the structure of JavaScript code
- Extract features from AST![ref1]

**Generation of N-gram features![ref1]**

![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.005.jpeg)

AST of Javascript code can be obtained by “Esprima.Parse” in Json format     Example of javascript code

`              `var answer = 6\*7

`              `function test() 

`              `{

`                    `alert(“hello world”);

`             `}![ref1]

**Abstract Syntax Tree![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.006.jpeg)![ref1]**

**Generation of N-gram![ref1]**

![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.007.jpeg)

**Feature selection**

- Information gain can be used for feature selection

![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.008.png)

- Top 800 key features can be used for training the model![ref1]

**Experimental Results![ref1]**

![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.009.png)

![](Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.010.png)

**Conclusion**

- Code injection attacks in hybrid applications are detected using a convolutional neural network (CNN). 
- Abstract syntax tree is constructed from JavaScript code of application. Then, Features are extracted from it. 
- Features are selected using information gain and chi square test feature selection technique. 
- The class imbalance problem is tackled by SMOTE data sampling method. 
- CNN is used to train the preprocessed data to predict whether a hybrid application as normal or vulnerable. 
- Experiments are conducted on 85 mobile apps downloaded from Google play store. 
- Classification accuracy of CNN is compared with machine learning models such as NB, Linear SVC and KNN. 
- CNN is able to provide better prediction accuracy for code injection attacks in hybrid applications. Static analysis of hybrid apps are considered in this work.![ref1]

[ref1]: Aspose.Words.27d199cc-b147-4352-98d3-390c5adb95d0.003.png
