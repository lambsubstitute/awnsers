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
Before I talk about the solution side I would like to explain why their are two projects in the folder. Understanding your requirment for the demonstration of c# and Specflow skills I wanted to provide that to you. However it has been a long time since I have used specflow (lets just say it was somewhere early in version 1) and just about as long since I have written any c#. Given that I wanted to also provide something a little more familiare to myself in watir, where I can demonstrate concepts and good use of the tools like cucumber. Another choice on using both of these was to incorporate the BDD scenarios as proper cucumber features. 
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

__**SpecFlow**__

Although I spent longer on this project, there are a lot more things I could have done better with more time (mostly reading up and refamiliarizing myself). Some of these include:
* **Use of sleeps.**
Use of sleeps is an anti-patten for test automation, but I could not find a way for it to wait for button/link in the time.
* **No page object model used.**
I did not have time to look up how this is usually implemented in c#. 
* **Lookups not using data-test-id.**
I could not find how to build custom lookups using these, and wanted to avoid using xpath to locate on these specifically. 

**How to run**

To run this project, please unzip and open in visual studio, and then run the tests. All the dependencies should be provided. 



__**Watir**__

I choose to do this in addition to the SpecFlow to show my knowledge and use of concepts such as Page Object model, where I am more familiare. The following is a diagram of the model I have used:
```
 ---->>> Cucucmber feature file: holds the scenarios and steps, these call the step definitions
   |
   |
 ---->>> Step definitions: clean step definitions, we conduct assertions and expectations at this level by calling the helpers
   |
   |
 ---->>> Helpers: using page objects user flows can be built, conditional logic about flows can also be added here. most of the complicated work will be done at this level. if the logical flow of functionality is to be changed it can be handled here
   |
   |
 ---->> Page objects: UI Interactions level, here we have the pure interactions that keep element identifiers for specific pages or page areas, which cuts down code reuse and improves maintainability
 ```
**How to run**
You will need to install Ruby 2.4.x (this was written on 2.4.1p111).
Install the ruby gem bundler using the command `gem install bundler`.
Once installed navigate to the root of the test folder, and run `bundler install` which should install all the required gems.
To run the tests, navigate to the 'test' folder and run the command `rake search`. Alternatively you can run the tests with the command `cucumber`.
 


## Question 2 
I dont know if it counts as a trend, but the introduction of new automation solutions on to the market that dont use selenium is interesting. Although they have there limitations or costs, it will be interesting to see how they develop moving forward. The w3c recomendation paper for Selenium is some interesting news from this June and will hopefully add some needed standadisation after all the time it has been around.  

## 3. 
If the system under test had no test automation coverage, The first steps would be to establish some tests around the business critical flows. These include registration, search, ordering, etc, the flows where most of the systems traffic is and the business money is made. Secondly I would look for any particular areas of the code that are not well maintained and/or are messy and hard to work on. Discussing with the developers is usually a pretty good way to sniff the smelly code out as they will usualy know them intemitely. Another way of identifying these area can be to look for areas of the system that have a higher bug rate. It can be important to get test coverage around these areas as well. 
All of the above is a pragamatic approach to the question at hand, but a lot would depend on the amount of time that could be spent on the system, and how much trust there is in the functionlaity that is already there. If there is a low confidence then it would require extra time to validate scenarios are correct and that tests are not being built around incorrect behaviour, which may not look like a bug is still incorrect from the businesses perspective.

## 4. 
Before leaving the uk 2 years ago I was a frequent user of Just Eat, but obviously I am unaware of how the sites functionality has improved in that time. So my suggestions may be a little dated however, driver tracking and meal status are two features that I would have enjoyed very much when using your service. Logistically thou i can understand how this could be tricky and require restaurant envolvement to achieve.  

## 5. 
```
{"name":"Keith Ford", 
 "age" : 37, 
 "hobbies" : ["Reading", "Arsenal", "Ancient Civilisations", "Travel", "TV and Movies"],
 "MentalAttributes" : {"Openness" : 8, "Conscientiousness" : 8, "Extraversion" : 8, "Agreeableness" : 8}
}
```
