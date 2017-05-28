# cppcast_notes

Notes for CpCast.




## Brief guest introduction

Richel Bilderbeek ('Re-shell builder-bake') is a C++ developer for 17 years.
He is mostly interested in what the literature has to say about good C++ practices, 
then teaching children and to adults, additionally
writing articles, blog posts and tutorials. In his professional life, 
he is a PhD in theoretical biology.

## Guest introduction

Richel ...

 * programs since the age of 8, by following an adult programming course in GW-BASIC
 * switched to QBasic at the age of 10
 * fell in love with a snippet of the Doom C++ source code
 * switched to C++ at the age of 20 at the university
 * set up and taught a C++ course there
 * discovered the literature (Meyers, Sutter, Alexandrescu)
 * collected all advice and put it online ([a page about const](http://richelbilderbeek.nl/CppConst.htm))
 * discovered GitHub, [approx 700 GitHubs](https://github.com/richelbilderbeek)
 * started teaching to kids and adults: [Arduino](https://github.com/richelbilderbeek/ArduinoCourse), [Urho3D, SFML, Processing, Scratch](https://github.com/richelbilderbeek/Dojo)
 * became a PhD in science, [university page](http://www.rug.nl/staff/r.j.c.bilderbeek/research)
 * wants to reach out more, [blog post at Arne Metz](https://arne-mertz.de/2017/04/continuous-integration-travis-ci/)

## Travis CI

 * What made you start?
 * What is it?
 * Why use it?

### What made you start using Travis CI?

 * started because it would be good practice
 * I already did TDD, [and TDD works, according to Uncle Bob](http://programmer.97things.oreilly.com/wiki/index.php/The_Three_Laws_of_Test-Driven_Development)
 * Recommended by [97 things every programmer should know](http://programmer.97things.oreilly.com/wiki/index.php/97_Things_Every_Programmer_Should_Know)
 * There was a scientist that also used it, [RPANDA package](https://github.com/hmorlon/PANDA)

### What is Travis CI?

 * a continuous integration service
 * push to GitHub and it does whatever you told it to
 * uses a `.travis.yml` script

### Why use Travis CI?

 * because it is supposed to be good practice to do so
 * no need to manually start your tests (unit tests, profiling, memory leaks, data races, etc)
 * ensures build is reproducible
 * Pull Requests get tested before merging
 * a badge of quality

## Good practices. Why follow them?

 * Because the experts know better than most
 * Every time I deviated from the advice, I regretted it
   * Writing a custom testing framework
   * YAGNI: Adding Boost.Signal2 to every class
   * Using boost::shared_ptr everywhere
 * Shows humility: I am not an expert programmer. Even Stroustrup does not claim this. Sean Parent makes you feel this
 * Shows being open to others' opinions: 
   * I've changed my programming style multiple times
     1. `void f(const double& x)` to `void f(const double x)`
     2. returning `T` to `const T`, Scott Meyers. Effective C++ (3rd edition). Item 2
     3. returning `const T` to `T`, Scott Meyers. Effective Modern C++
   * I've changed the case of my code multiple times, from `ThisWay` to `thatWay` to `this_way`
 * Show being social
   * Recognition of preferred ways to do things, e.g. `pimpl`: C++ Core Guidelines
   * Naming variables, functions, classes makes the code communicate better, Kevlin Henney

##  Good practices and Travis CI

 * Practice what you preach  
 * Measure that it *is* a good practice
 * Continuous integration amplifies many other good practices
   * Continuous profiling: find when you unknowingly introduce a speed bottleneck
   * 

## Teaching

   * Humble, open, admit errors
   * Volunteer
   * To kids and adults
   * Tutorials
     * Boost.Graph tutorial
     * Travis CI tutorial
   * Kate Gregory 'Stop teaching C', [her CppCon 2015 presentation](https://www.youtube.com/watch?v=YnWhqhNdYyk)

## Teaching and Travis CI

   * Forcing students to use good practices
     * OCLint, gcov, gprof, cppcheck, valgrind
   * Tutorials
     * aspell, proselint
## People

 * Niall Douglas (Boost.AFIO v2 and Boost Outcome), Stroustrup, Sutter, Meyer, Alexandrescu
 * Humble, open, admit errors

## People and Travis CI

## Science

 * Theoretical biology
 * Humble, open, admit errors

## Science and Travis CI

 * Why are the C++ good practices ignored?
 * Makes research reproducible

## Future ideas


## 

103.

Rob Irving
Jason Turner


 * Introduction: who is he? brief
 * News: comment on it


Niall Douglas: Boost.AFIO v2 and Boost Outcome









## Email sent to Rob and Jason

The topic:

Travis CI is a continuous integration service. It will run any script every time you push your code to an online code repository. For example, it can check if your code compiles. It does so in a virtualized environment, using Docker, resulting in reproducible builds. But Travis can do anything you can put in a bash script. Examples are: running test suites, measuring code coverage, profiling, static code analysis, checking the coding style, checking for memory leaks, checking for synchonization errors, and more. My favorite setup, https://github.com/richelbilderbeek/the_richel_setup , has a C++ project checked in all those aspects. Not only does Travis CI safeguard the quality of your project, I use it for teaching as well: I supply my students with a prepared GitHub and let Travis make its suggestions.

My bio:

I started programming at the age of eight in GW-BASIC by following a course for adults, with an official exam that I passed with flying colors. I made the switch to QBasic and developed some games, some of which were twenty players games (on one keyboard!). 

At the age of twenty, I made the switch to C++ to build simulations in the field of theoretical biology. In my spare time, I kept creating games, but also got my first paid C++ projects. I started reading the C++ literature and changed my style multiple times due to this: I wanted to do C++ in the best way possible. I started giving C++ courses, trainings and got active on the Programmers' Heaven forum. I wrote a 2000+ wikipedia about C++ at Codepedia ( www.codepedia.com ) that gives minimal examples and references to the literature. When the Codepedia changed its layout that my articles looked bad, I ported the content to my personal HTML website ( www.richelbilderbeek.nl ), growing to 3000+ pages about C++.  

git and GitHub had a massive impact on my workflow and I now have 600+ GitHub repositories. I ported my 3000+ C++ pages to GitHub ( https://github.com/richelbilderbeek/cpp/tree/master/content ) and am still in the process of doing so. 

As a volunteer, I started to additionally teach kids programming in Scratch, Processing and C++ ( https://github.com/richelbilderbeek/Dojo ), also on Arduino ( https://github.com/richelbilderbeek/ArduinoCourse ). After approx three years, I have around thirty students aged 7-18 that visit my cheap (1 euro per evening) courses.

My programming style is mostly influenced by Stroustrup, Meyers, Sutter, Alexandrescu (all have been on your show) and Kevlin Henney. Kate Gregory (she has been on your show as well) has been a major support in how I teach C++. 

Travis CI, and continuous integration in general, had another major impact in the way I work. I have about 200+ GitHub repos checked by Travis CI and AppVeyor. I have added Travis CI support to approx 20+ GitHub repos of tools I used. I am in the process of writing a tutorial about this ( https://github.com/richelbilderbeek/travis_cpp_tutorial ), but already produced some blog posts about it: one in C++ for Arne Metz's (he has been a guest in your show) Simplify C++ blog ( https://arne-mertz.de/2017/04/continuous-integration-travis-ci/ ) and one about R in the SDJournal ( https://github.com/richelbilderbeek/sdj_raising_your_code_to_professional_standards ). 

One of the thing that puzzles me the most, is how academia mostly does not follow the best practices in programming. Where scientist are trying to unravel the truth, it appears unimportant if the code used is correct. It has been estimated that 20% of all publications in my field are based on software bugs. Few (but luckily more and more) academic simulations use GitHub (most code has to be requested by email) and less have tests. And where communication of your ideas is one of the most important skills as a scientist, readable code, nor documentation of it, somehow is not included. I can be amazed by coding styles perpendicular to the C++ Core Guidelines and these deviations defended (even 'void main') by the most successful scientists. I fight to make academia more reliable and social by putting code on GitHub and adding Travis CI. I am happy to see that this sometimes works out great!

Three years ago, I started to use the R programming language and I am now the R User Group Groningen (the city where I live) coordinator. Also the R community can benefit from good programming practices, for example, from Hadley Wickham. From R I learned what most students expect programming to be: it should be easy to let the computer just do something, and debugging is just OK. R is great for that! I prefer the other way around: compiling should be strict, so run-time debugging can be avoided, which is where C++ shines (the Boost.Graph library is great in that aspect)! 

I have written quite some tutorials, most are still growing organically: 

https://github.com/richelbilderbeek/BoostGraphTutorial
A well-connected C++14 Boost.Graph tutorial

https://github.com/richelbilderbeek/travis_cpp_tutorial
Tutorial how to use Travis CI with C++

https://github.com/richelbilderbeek/mxe_tutorial
Tutorial about the MXE cross-compiling environment

https://github.com/richelbilderbeek/testing_cpp_gui_applications_tutorial
Tutorial about testing C++ GUI applications

https://github.com/richelbilderbeek/travis_r_tutorial
Tutorial about using Travis CI in R projects

https://github.com/richelbilderbeek/appveyor_cpp_tutorial
Tutorial how to use AppVeyor with C++

Recently I discovered my 17 years of C++ experience is really something. I consider myself a mediocre programmer that just follows the best practices. But there are plenty of beginner C++ programmers that can benefit from experienced C++ programmers like me. This insight made me reach out to CppCast and blogs.

Future goals are to reach out more, try to improve academia's coding practices and keep teaching my minor (and adult) students C++ in the correct way.
