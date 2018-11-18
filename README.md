# awnsers
## Question 1
```
Time Spent
SpecFlow: 3 Hours 
Watir: 1 Hour
Writeup: 1 Hour
-----------------
Total: 5 Hours
```
Before I talk about the solution side I would like to explain why their are two projects in the folder. Understanding your requirment for the demonstration of c# and Specflow skills I wanted to provide that to you. However it has been a long time since I have used specflow (lets just say it was somewhere early in version 1) and just about as long since I have written any c#. Given that I wanted to also provide something a little more familiare to myself in watir, where I can demonstrate concepts and good use of the tools like cucumber. 
That being said I will go through common improvements I would make given the time (or if it was being deployed to a production environment). 

__Common Improvements__

* **cleaner html lookups on some entries.** 
This is espcially true in the SpecFlow example. For watir I was able to build the custom lookups in the `env.rb` for the `data-test-id`'s, but for a few elements I still had to use segments of class attributes, which could change. Given the time I would like to have looked for better elements or added the custom data tags to said elements.  
* **Better browser Support and cleanup.**
Currently both test suites only support Firefox and Chrome. I would have like to introduce IE, Edge, and maybe Safari for both solutions. The SepecFlow tests suffer from the browsers not being shut down after the tests have completed, something which helped when debugging them but is not useful for CI. 
* **Screenshotting and other reporting.**
Neither test suite reports failures nicley or creates any test reports, screenshots, or other debugging information besides what is provided by the console. If I had the time I would have liked to include Allure reporting in to both projects, although this is not something I have done before in these langauges, I have done it with selenium JVM tests successfully. 
* **Ability to run tests in parralel.**
Neither test has this capacity
* **Fragile tests due to data dependency.**
The tests have no ability to set the data up first and as such there is no garuntee it will always be in the system under tests resulting in false failures. 

**SpecFlow**
Although I spent longer on this project, there are a lot more things I could have done better with more time (mostly reading up and refamiliarizing myself). Some of these include:
* **Use of sleeps.**
Use of sleeps is an anti-patten for test automation, but I could not find a way for it to wait for button/link in the time.
* **No page object model used.**
I did not have time to look up how this is usually implemented in c#. 
* **Lookups not using data-test-id.**
I could not find how to build custom lookups using these, and wanted to avoid using xpath to locate on these specifically. 



## Question 2 


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
