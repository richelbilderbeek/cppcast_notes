# cppcast_notes

[![Travis CI logo](TravisCI.png)](https://travis-ci.org)

[![Build Status](https://travis-ci.org/richelbilderbeek/cppcast_notes.svg?branch=master)](https://travis-ci.org/richelbilderbeek/cppcast_notes)

Shownotes for CppCast episode 103.

 * Host: Rob Irving
 * Co-Host: Jason Turner
 * Guest: Richel Bilderbeek ('Re-shell builder-bake')

## Brief guest introduction

Richel Bilderbeek is a C++ developer for 17 years.
He is mostly interested in what the literature has to say about good C++ practices, 
then teaching children and to adults, additionally
writing articles, blog posts and tutorials. In his professional life, 
he is a PhD in theoretical biology.


## News discussion

 * Writing a Really, Really Fast JSON Parser - https://chadaustin.me/2017/05/writing-a-really-really-fast-json-parser/
  Boost.ProperyTree has a JSON parsers
 * C++ Online Compilers - https://arne-mertz.de/2017/05/online-compilers/
 * Looking for Proofreaders for my new Book: Concurrency with Modern C++ - http://www.modernescpp.com/index.php/looking-for-proofreaders-for-my-new-book-concurrency-with-modern-c. Rainer Grimm

## Guest introduction

Richel 

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

## I think a lot of our listeners may have at least heard of Travis CI, for those that don't though or those who have just seen a badge on a github repo and don't know anything else why don't you tell us what Travis is

 * a continuous integration service
 * push to GitHub and it does whatever you told it to
 * uses a `.travis.yml` script
 
## Why should C++ developers use Travis?

 * because it is supposed to be good practice to do so
 * no need to manually start your tests (unit tests, profiling, memory leaks, data races, etc)
 * ensures build is reproducible
 * Pull Requests get tested before merging
 * many diagnostics can be added at low cost
 * to learn/teach
 * a badge of quality

## What got you interested in Travis?

 * Friend from hackerspace used Jenkins
 * a good practice
 * I already did TDD, [and TDD works, according to Uncle Bob](http://programmer.97things.oreilly.com/wiki/index.php/The_Three_Laws_of_Test-Driven_Development)
 * Recommended by [97 things every programmer should know](http://programmer.97things.oreilly.com/wiki/index.php/97_Things_Every_Programmer_Should_Know)
 * There was a scientist that also used it, [RPANDA package](https://github.com/hmorlon/PANDA)

## What can you do with Travis? CI Builds, unit tests, more?

 * Testing the build
 * Running unit tests
 * Everything you want to do automatically

## What scripting language are Travis scripts written in?

 * `yml`: Yet Another Markup Language
 * indentation matters
 * bash commands

## Do you use other tools with Travis, like cppcheck / clang-tidy?

 * All tools I can get to work
   * cppcheck
   * gcov
   * OCLint, similar to metrix++
   * gprof and perf
   * helgrind (thread errors)
   * memcheck (memory leaks)
   * libfuzzer
 * With mixed success
   * clang-tidy
   * clang-modernize
 * Without success
   * Coverity Scan
 * Misc
   * aspell, proselint

## Sometimes, git and GitHub are called 'transformative tools', as they change your workflow. Would you consider CI be that as well?

 * Yes
 * I dislike doing things manually
 * Continuous integration amplifies many other good practices
   * Measuring code coverage changes your architecture
   * Adding style detection tools changes your coding style
   * Automate profiling shows that indeed most functions need not to be speed improved

## What OS's and platforms does Travis support?

 * GNU/Linux, MacOS (, Android)
 * Windows: use AppVeyor
 * Many languages

## Tell us a bit more about your professional life, how is C++ used in theoretical biology?

 * Theoretical biology: mathematics, computer simulations
 * Examples
   * MSc project: earthworms
   * PhD project: speciation models
 * Reproducible in theory
   * 20% of articles from a software bug
   * GitHub and Travis help ensure reproducability and quality
   * Most scientists do not care about the C++ good practices

## Your github profile mentions that you teach Arduino programming, how much C++ do you teach with the Arduino?

 * Arduino-style C++: 
  * no STL
  * arrays
  * const global variables

OTOH, I also teach a programming course, in which we teach SFML and Urho3D

 * Similar to Kate Gregory 'Stop teaching C', [her CppCon 2015 presentation](https://www.youtube.com/watch?v=YnWhqhNdYyk)
 * Accelerated C++, Andrew Koenig & Barbara Moo
 * Programming, Stroustrup
 * C++ Core Guidelines 
 * Until they need a feature

## Are your students receptive to C++?

 * Minor kids
   * sent email: 'I am not using it now, but will probably be okay', yet he is programming Arduino and playing with OpenGL examples in Qt?
   * they are interested in what you can do with it
 * University students
   * they have to learn it, due to academic culture
   * 'hard': compile time error feels worse than a run-time error 

## Are there similar continuous integration services?

 * AppVeyor (Windows)
 * Decent CI, Codeship, Jenkins, Wercker, etc.

## Is there a feature you miss in Travis CI?

 * Testing desktop application GUIs
   * xdotools, Sikuli, LDTP2

## Where would you suggest to start with Travis CI?

 * Use the Travis CI documentation
 * Find minimal example: [travis_cpp_tutorial statuses](https://github.com/richelbilderbeek/travis_cpp_tutorial/blob/master/statuses.md)
 * Tutorial: [travis_cpp_tutorial](https://github.com/richelbilderbeek/travis_cpp_tutorial)

# My own notes

These I could not put in the interview

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

## Teaching

 * Parents were ballroom dancing teachers
 * Set up a C++ programming course at the university, with C++ Builder, for theoretical biologists
 * Graduated as a teacher in biology, taught biology, chemistry, physics and stagecraft at a secondary school
 * Collected all C++ advice on [http://richelbilderbeek.nl](my personal website), now [on GitHub](https://github.com/richelbilderbeek/cpp)
   * Stroustrup: humble, condensed
   * Meyers: funny, convincing
   * Sutter and Alexandrescu: funny, convincing
   * Sean Parent: deep detailed knowledge
   * Kevlin Henney: naming things well
   * Kate Gregory 'Stop teaching C', [her CppCon 2015 presentation](https://www.youtube.com/watch?v=YnWhqhNdYyk)
 * Set up two courses to teach Arduino and programming
   * Dutch teaching material
 * [Articles](https://github.com/richelbilderbeek/articles): first on my website only, just recently on [Arne Metz's Simplify C++ blog](https://arne-mertz.de/2017/04/continuous-integration-travis-ci/)
 * Tutorials
   * [Boost.Graph tutorial](https://github.com/richelbilderbeek/BoostGraphTutorial): 90%
   * [Travis CI tutorial](https://github.com/richelbilderbeek/travis_cpp_tutorial): 70%
   * [Tutorial about the MXE cross-compiling environment](https://github.com/richelbilderbeek/mxe_tutorial): 50%
   * [Tutorial about testing C++ GUI applications](https://github.com/richelbilderbeek/testing_cpp_gui_applications_tutorial): 50%
   * [Tutorial about using Travis CI in R projects](https://github.com/richelbilderbeek/travis_r_tutorial): 70%
   * [Tutorial how to use AppVeyor with C++](https://github.com/richelbilderbeek/appveyor_cpp_tutorial): 30%

## Teaching and Travis CI

 * Force students to use good practices
   * OCLint: style must follow the guidelines
   * gcov: check code coverage: must be high, unused code can be removed
   * gprof: show run-time speed: only improve speed of functions where it matters
   * cppcheck: static type checking
   * valgrind: memory leaks, data races

## Science and Travis CI

 * GitHub (and Travis CI) facilitates research being open
 * Travis CI facilitates research being reproducible
 * I like to add Travis CI to academic GitHubs

## Future goals

 * Reach out more
 * Try to improve academia's coding practices 
 * Keep teaching correct C++
