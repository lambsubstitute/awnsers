# Answers
```
Time Spent
SpecFlow: 3 Hours 
Watir: 1 Hour
Writeup: 1 Hour
-----------------
Total: 5 Hours
```
## Question 1
I have completed a simple solution using c# and SpecFlow. I am a little out of practice having not worked with either since 2011 and felt it did not demonstrate my abilities sufficiently. This is why I have also included a second test suite using ruby and watir.  I am more familiar with this tool set and thought it would demonstrate my knowledge of concepts such as the page object model, and the use of cucumber. I will now go through common improvements I would make given the time (or if it was being deployed to a production environment).

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
The tests have no ability to set the data up first and as such there is no guarantee it will always be in the system under tests resulting in false failures. 

### SpecFlow

There are some things I would have done better with more time. Some of these include:
* **Use of sleeps.**
Use of sleeps is an anti-patten for test automation.
* **No page object model used.**
Although I did try to cut code reuse down within the step file, with helper methods. 
* **Lookups not using data-test-id.**
I would like to have added custom lookups on these. 

#### How to run
To run this project, please unzip and navigate to the SpecFlow folder. With visual studio 2017 open the solution found in the SpecFlow folder called `menulogSearch.sln`. The tests can then be from the Visual studio options menu. All the dependencies should be provided in the packages folder. 



### Watir 

I choose to do this to show my knowledge and use of concepts such as Page Object model. The following is a diagram of the model I have used:
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
#### How to run
You will need to install Ruby 2.4.x (this was written on 2.4.1p111).
Install the ruby gem bundler using the command `gem install bundler`.
Once installed navigate to the root of the test folder, and run `bundler install` which should install all the required gems.
To run the tests, navigate to the 'test' folder and run the command `rake search`. Alternatively you can run the tests with the command `cucumber`.
 
## Question 2 
The introduction of new automation solutions on to the market that don't use selenium is interesting. Although they have their limitations or costs, it will be interesting to see how they develop moving forward. The w3c recomendation paper for Selenium is some interesting news from this June and will hopefully add some needed standardisation after all the time it has been around.  

## Question 3 
If the system under test had no test automation coverage; the first steps would be to establish some tests around the business critical flows. These include registration, search, ordering, etc, the flows where most of the systems traffic is and the business money is made. Secondly I would look for any particular areas of the code that are not well maintained and/or are messy and hard to work on. Discussing with the developers is usually a pretty good way to sniff the smelly code out as they will usualy know them intemitely. Another way of identifying these areas can be to look for parts of the system that have a higher bug rate. It can be important to get test coverage around these areas as well. 
All of the above is a pragamatic approach to the question at hand, but a lot would depend on the amount of time that could be spent on the system, and how much trust there is in the functionlaity that is already there. If there is low confidence then it would require extra time to validate scenarios so that tests are not being built around incorrect behaviour, which may not look like a bug, but is still incorrect from the businesses perspective.

## Question 4 
Before leaving the UK 2 years ago I was a frequent user of Just Eat, but obviously I am unaware of how the sites functionality has improved in that time. So my suggestions may be a little dated however, driver tracking and meal status are two features that I would have enjoyed very much when using your service. Logistically thou i can understand how this could be tricky and require restaurant involvement to achieve.  

## Question 5 
```
{"Keith Ford":{ 
   "age" : 37, 
   "hobbies" : ["Reading", "Arsenal", "Ancient Civilisations", "Travel", "TV and Movies"],
   "favouriteTV" : ["Rick & Morty", "Black Mirror", "South Park", "The Venture Bros"],
   "mentalAttributes" : {
                           "Openness" : 8, 
                           "Conscientiousness" : 9, 
                           "Extraversion" : 7, 
                           "Agreeableness" : 8
                        }
 }
}
```
