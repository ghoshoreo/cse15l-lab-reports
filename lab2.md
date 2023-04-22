Lab Report 2
=============
Welcome to Lab Report 2 of CSE 15L. This lab report is divided into three parts, reflecting the three tasks for this lab report.

Task 1
------

After writing the required code for `StringServer`, we have to start a server session at localhost. 

![Image](localhost_connect.png)

Given below is the code for `StringServer`, followed by two screenshots of using `/add-message`.

![Image](stringserver.png)

*Screenshot 1*

![Image](localhost_str_1.png)

*Screenshot 2*

![Image](localhost_str_2.png)

Let us examine each of the screenshots in detail.

**Screenshot 1**

* The method `handleRequest` in my code is called. Its argument is `url` of class `URI`. There are two fields in that method, namely `message` and `parameters`. The method `handleRequest` calls additional methods. These methods are `getPath()`, `equals()`, `split()`, and `getQuery()`.

* The argument `new URI(http://localhost:5000/add-message?s="Hello")` is passed as the field `url` to the method `handleRequest`. The field `parameters` stores the array of Strings value `{"s", ""Hello""}`. The field `message` returns the String value `""Hello"\n"`.

* Due to passing the request `/add-message?s="Hello"`, the field `parameters` was initialized and the value of the field `message` was initialized and subsequently changed. The value of the field `message` was initialized to the empty String `""`. The value of the field  `parameters` was initialized to the array of Strings value `{"s", ""Hello""}`. Upon completion of the method run, the value of the field `message` is changed to the String value  `""Hello"\n"`. 

**Screenshot 2**

* Similarly, the method `handleRequest` in my code is called. Its argument is `url` of class `URI`. There are two fields in that method, namely `message` and `parameters`. The method `handleRequest` calls additional methods. These methods are `getPath()`, `equals()`, `split()`, and `getQuery()`.

* The argument `new URI(http://localhost:5000/add-message?s=How%20are%20you)` is passed as the field `url` to the method `handleRequest`. The field `parameters` stores the array of Strings value `{"s", "How are you"}`. The field `message` returns the String value `""Hello"\nHow are you\n"`.

* Due to passing the request `/add-message?s=How%20are%20you`, the field `parameters` was initialized and the value of the field `message` was initialized and subsequently changed. The value of the field `message` was initialized to the empty String `""`. The value of the field  `parameters` was initialized to the array of Strings value `{"s", "How are you"}`. Upon completion of the method run, the value of the field `message` is changed to the String value  `""Hello"\nHow are you\n"`. 
