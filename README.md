# awnsers
## Question 1
```
Time Spent
SpecFlow: 3 Hours 
Watir: 1 Hour
-----------------
Total: 4 Hours
```
Before I talk about the solution side I would like to explain why their are two projects in the folder. Understanding your requirment for the demonstration of c# and Specflow skills I wanted to provide that to you. However it has been a long time since I have used specflow (lets just say it was somewhere early in version 1) and just about as long since I have written any c#. Given that I wanted to also provide something a little more familiare to myself in watir, where I can demonstrate concepts and good use of the tools like cucumber. 
That being said I will go through common improvements I would make given the time (or if it was being deployed to a production environment). 

__Common Improvements__

* **cleaner html lookups on some entries.** 
This is espcially true in the SpecFlow example. For watir I was able to build the custom lookups in the `env.rb`, but for a few elements I still had to use segments of class attributes, which could change. Given the time I would like to have looked for better elements or added the custom data tags to said elements.  
* **Better browser Support and cleanup.**
Currently both test suites only support Firefox and Chrome. I would have like to introduce IE, Edge, and maybe Safari for both solutions. The SepecFlow tests suffer from the browsers not being shut down after the tests have completed, something which helped when debugging them but is not useful for CI. 
* **Screenshotting and other reporting.**
Neither test suite reports failures nicley or creates any test reports, screenshots, or other debugging information besides what is provided by the console. If I had the time I would have liked to include Allure reporting in to both projects, although this is not something I have done before, I have done it with selenium JVM tests successfully. 

## 2. 


## 3. 

## 4. 

## 5. 
```
{"name":"Keith Ford", 
 "age" : 37, 
 "hobbies" : ["Development","Arsenal","Ancient Civilisations", "Travel"],
 "MentalAttributes" : {"Openness" : 8, "Conscientiousness" : 8, "Extraversion" : 8, "Agreeableness" : 8}
}
```
