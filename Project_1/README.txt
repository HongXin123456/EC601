Topic: Statically analyze Android applications and build a classifier that distinguishes malicious from benign applications


        We want to build a static code analyzer for complied Android applications to represent each app as a feature vector. This analyzer obtains a set of labeled malicious and benign Android apps. It will also extract the feature vectors. Then, we train an ML-classifier with the resulting vectors and evaluate the performance of the classifier. This analyzer is relatively inexpensive to implement and very useful for many Tech companies. For example, a static code analyzer helps security analysts to narrow down on threats or weaknesses detected in the early or final stages of development, before the beginning of the software testing phase. More specifically, static code analysts can be set up to automatically find the exact weakness of codes, such as Apps, classes, and methods. Therefore, analysts allow developers to spend less time to find and fix the errors. This directly saves companies’ assets and improves customer experience. To narrow down the scope of this project, I will focus on building a static code analyzer for Android applications.
After reviewing a few existing tools, I decide to choose Androguard. This tool is free and can be used purely as a library. It allows developers to use the cli or graphical frontend for androguard. Here is the reference link for installing and using detekt, https://github.com/detekt/detekt.
To start this project, I will implement the detekt library on a simple Andriod App that contains no bugs. This is the control group that ensures everything works as expected. After that, I will duplicate this App 10 times and randomly throw in some errors in the same class and run Androguard on all the Apps to extract feature vectors. Then, I will train a Machine Learning classifier with those vectors that will be assigned labels. I also want to use detekt and create log files. I can use NLP to parse and train those logs. At this early stage, I cannot decide which classifiers to be used, but Naive Bayes and Random Forest are good places to start. In order to generate more vectors for machine learning. It is very likely that later on in this project, I will design a function to create random errors in the designated class.




Static analysis tools
Improve product quality: detecting error before entering to the code base
Code quality: analyze control flow, analyze data flow
Stand-alone utility








Detekt
Highly configurable analysis tool for Kotlin
Checks for code complexity, code smell, formatting
Can include ktlint checks