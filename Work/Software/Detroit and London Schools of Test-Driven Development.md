---
ressource: 📰 Article
link: https://blog.devgenius.io/detroit-and-london-schools-of-test-driven-development-3d2f8dca71e5
trello: https://trello.com/c/FPiDSMA0/128-detroit-and-london-schools-of-test-driven-development
---
#Ressource/Article📰 

[[London School of TDD]]
[[Detroit School of TDD (aka. Chicago)]]

# Introduction

**[[Test-Driven Development]] (TDD)** has become one of the core tools in the toolbox of a modern developer. Its practice is often considered as a manifestation of professionalism in software.

![](https://miro.medium.com/v2/resize:fit:709/1*QnnqbhOh_VaNpJXsNyURfg.jpeg)

Test-Driven Development cycle

I’ve been doing TDD for over a decade. Every project I worked on acquired a slightly different approach. I can easily name specific techniques, like state or interaction testing, test doubles, mocking, growing application bottom-up, or broad-brush design. But there was always something missing, a common term which would group these sometimes contradictory techniques, and put clarity on benefits or risks associated with a given technique. One conversation (hi David!) has changed it all. This is how I’ve learnt about **Detroit and London Schools (or styles) of TDD**, and decided to dive deeper to discover more. A practice of TDD is a straightforward technique, although the devil is in the details.

In this post, I will outline the main differences between the two schools of Test-Driven Development, look into specific techniques forming the practice, analyse how they approach problem-solving, and suggest how to mitigate risks arising from using them. I aim to stay unopinionated, hoping it’s not a futile endeavour (who has no strong opinions?). Feel free to challenge me, and show where I’m wrong.

# A bit of history or “location, location, location”

![](https://miro.medium.com/v2/resize:fit:354/1*pNvNrtEonSjOa-EObUIGHg.jpeg)

Test-Driven Development originated in the late nineties in Detroit, out of the ashes of the Chrysler Comprehensive Compensation System. Kent Beck, the lead engineer on the project, codified the technique and outlined the practice in **_Test-Driven Development By Example_** book. TDD became an essential best practice in **Extreme Programming (XP)** methodology, which built the foundations of the emerging Agile movement. Specifics of the approach promoted by Beck became recognised as **the [[Detroit School of TDD (aka. Chicago) | Detroit]], or the Classicist, School of TDD**. Prominent representatives are also Robert C. Martin (Uncle Bob), Ron Jeffries, and Martin Fowler.

![](https://miro.medium.com/v2/resize:fit:354/1*OtGEdiEE2CmwF_4MTD0yvw.jpeg)

Test-Driven Development quickly gained popularity. London for centuries provided fertile soil for thought-provoking ideas. In the early 2000s, London’s Extreme Tuesday Club (XTC) was formed. It attracted the avant-garde of UK’s TDD/XP practitioners and provided a great community to share experiences, techniques, and ideas. It helped Steve Freeman and Nat Pryce to distil their vision of TDD which resulted in publishing **_Growing Object-Oriented Software Guided By Test_**. Next to Kent Beck’s book, it quickly became the second most important publication on Test-Driven Development. The style promoted in the book is known as **the [[London School of TDD]]**, sometimes labelled as **the Mockist**. It codifies and clarifies the technique of mock objects, not widely known before.

# Two paths to enlightenment

Both the Detroit and the London schools praise the benefits of TDD practice: steady incremental progress, elimination of fear, simplicity of design and quality of code. Nevertheless, they provide distinct guidelines on reaching TDD nirvana. I’ve grouped them into three areas:

- definition of the unit
- design and the test writing practice
- use of test doubles

Let’s dive in to see how different they are.

# The unit

Unit testing is a signature activity of TDD. What is the unit in unit testing?

In the Classicist world, **the unit is a module**. A module is a single class, just a function, or a set of closely related classes, which implement a particular functionality. It doesn’t matter how small and simple, or complex and full of inside collaborations it is. A module’s functionality is exposed by public exports (API). Hence, in the Detroit style, you write a test against the module.

In the London school, on the other hand, a unit test is often written with a single class in mind, hence **the unit tends to be a class**. If a class has collaborators they are mocked (the Mockist style, remember?), making dependent application layers detached. Use of mock objects enable this approach, and this is how tests likely to be written. On the other hand, nothing stops you from embracing the unit as a module if you think it’s more beneficial.

In the Detroit style, the **System Under Test (SUT)** grows with the application, making the unit test to operate on an expanding context. In the London style, the use of mocks in place of real collaborators makes the test setup small and the context limited.

# Emerging design and the practice of test writing

Application design is a complex subject. Traditionally teams approach it with a set of non-coding activities, like in-depth analysis, UML sketching, or extensive design sessions. TDD approach is almost the opposite. It is a design technique by itself. It lets the tests dictate the design of the system. It doesn’t mean that the architecture only comes from tests. The good architecture is designed over time, through iterations. It takes a while before you’ll finally settle with a good one. The way the schools of TDD approach the design is distinct and is expressed in the way you write your tests as well.

In the Detroit sense, I like to see it as digging deep. Focus on an exploration of the core logic with all its complexities from the very first moment. Don’t shy away from diving straight into it. If you need a collaborator, go and implement it, in the simplest possible way to get your test passing. Work on the vertical slices. Discover what lies behind and integrate early. Dig into the heart of the onion. Don’t worry about the breadth, it will come in time. Observe how the design emerges.

In the London style, your exploration starts by gaining a wider view first. Do a broad-brush design. Draw a few things first, not too many, just enough to get a mental model of the system. Explore API entry points, identify roles, responsibilities and key interactions between collaborators. Don’t dig deep, that’s not the point. Start from the top and work your way inwards. Focus on writing a test for the first layer. Mock your collaborators, committing to fleshing out their behaviour later. Once ready to move deeper, identify the next layer and repeat the process. Explore the onion’s layers, one by one. Eventually, you’ll get to the heart.

![The onion](https://miro.medium.com/v2/resize:fit:256/1*7dIUtkC0su4CPgtjaU2pzw.jpeg)

The Detroit style is an **inside-out** design process, while the London, **outside-in**. Can they influence the final design? There’s no evidence for it. The way the system is tested shapes its design in a short time. The more complete it gets the testing style’s influence fades. On the other hand, one could argue that _digging deep_ vs _working in layers_ results in a distinctly laid down system. This only could happen if the feature cycle is long. However, if the cycle is short and keeps producing small, but complete deliveries, I can’t see a big divergence in the design. Also, there’s much more to design than just the way you write your tests. More on this soon.

# Test doubles

![](https://miro.medium.com/v2/resize:fit:354/1*VWyDE-VZ-LCYvtRXnsXh8A.png)

The Detroit school argues: _if an object is hard to test, then it’s hard to use_. The London school goes a step further saying: _if a dependency is hard to mock, then it’s hard to use_. Both complement each other, setting some distinctions too.

While focusing on vertical slices, the Detroit style is not particularly concerned with the collaborations. Collaborations, as long as they are internal, are embraced and fully initialised in the testing harness. Test fixtures produce an almost complete system. This results in **no need for the extensive use of mocks** and it enables **state verification**. In effect, as unit tests expand over the full system, they become mini-acceptance tests. Although it does not mean you won’t need test doubles, ie mocks, if a collaborator gets awkward.

In the London approach, where the layer discovery takes precedence, mocks become bread and butter of the style. In the world where a unit is a class, it’s **more convenient to mock collaborators**. You draw only parts of interaction which are required for a specific test to pass. While it’s sensible to assert on the state, often you rely on **verifying interactions**. You want to make sure the code makes all relevant calls to its collaborators to achieve the desired goal, the results may manifest only down the line.

The Detroit style makes only a minimal need for end-to-end tests. Usually, you will need just a few to demonstrate the correct wiring of the integrated system. In the London style, if you end up with heavily mocked tests, the need for end-to-end tests is greater. They will provide much-needed confidence in the system, which can’t be guaranteed otherwise.

It’s worth mentioning that **_mock objects_** is a widely misunderstood technique and its use stirs the most heated debates. Mocks are not about ring-fencing code dependencies. It’s a tool in the process of test-driving system design. They help in delaying decisions you don’t want to take now. One way or another, below points are equally fair and don’t contradict each other.

> “Programmer tests should be sensitive to behaviour changes and insensitive to structural changes. (…) If I care about the order of operations, I’ve designed the system wrong” — Kent Beck (the Detroit School)
> 
> “If I have an object that has behaviour and I’m doing “Tell, Don’t Ask” then I can only test interactions.” — Steve Freeman (the London School)

# You’re Doing It Wrong!

![](https://miro.medium.com/v2/resize:fit:336/1*hHAkG1_09X79FocLUHdl6Q.jpeg)

Any tool or technique, no matter how smart, can be misused. It’s very easy to see everything as a nail if all you have is a hammer. The critique arises quickly. Instead let’s have a look on a few anti-patterns associated with styles and how to mitigate them. As it’s not about the technique but the fact that **_you’re doing it wrong!_**

# Detroit: My fixtures are too complex

_Having so much under test you get to copy fixture code into each test case. Your test examples are getting out of hands. Your tests become inflated, delicate, hard to read. Each little production code tweak forces you to change many tests._ **_You’re doing it wrong!_**

- It’s time to spend some time with your test code. Introduce common fixtures (factories, builders, object mothers) and reuse them across your tests. They should be expressed in the domain language and read well. You want them to tell you a story about how the system sticks together. Maybe you can not only simplify the test setup but the system itself?
- If it’s still too complex, perhaps your module is trying to do too much. Is there a problem with the design? Bring another pair of eyes and review it again.
- The quality of the test code is as important as the quality of the production code. It’s your documentation. Tests must be cheap to write, easy to read, simple to change.

# London: I spend more time fixing tests than writing production code

_You’re using mocks. Great. One mock here, another mock there. This mock returns another mock, hell yeah! You’re moving fast. Your tests are green. Everything is awesome. One day you have this great idea on how to make your app even simpler, without changing the functionality. It’s the day you don’t want to talk about. Everything falls. You can’t move. Every little change causes hundreds of tests to fail._ **_You’re doing it wrong!_**

- You’re suffering from the test-induced damage. Refactoring is a nightmare, the feature delivery dramatically slows down. Your mock-heavy tests are so tied to the implementation that every little change is a chunky sidequest. Time to grab your sword and face the beast!
- There’s one little detail someone forgot to tell you about mocks. Mocks are awesome for deferring decisions, but you shouldn’t leave too many mocks behind. Once you’ve got it all sorted, understood, implemented, why not to introduce a real collaborator instead of a mock? It might require a bigger refactoring, but hey, you’re gaining confidence here. Your unit tests become mini-acceptance tests. This is a win! It’s also a good occasion to review and maybe even delete some tests as you’re gaining more coverage with less. Oh, and you might not need so many end-to-end tests. What do you say about that?
- Ever scratched your head wondering what does the test actually assert? It’s so heavily mocked it’s hard to tell if it brings any value. Kill it. A friend you can’t trust is not a friend.
- Rule of thumb is: fewer mocks leads to more evolvable and bug-free system. Use mocks as long as they bring value. They should not stop you from moving forward. They should not stop you from refactoring. Keep them, as long as they help. The moment they start coming in the way, step back and have another look.

# Detroit or London: My design is not emerging, it’s a ball of mud…

_Test after test your system is getting more complicated, slipping out of your control. Where is this design supposed to emerge? I don’t see it! It’s only getting harder and harder to write the next test and keep other tests passing. I hate this Detroit/London school of TDD._ **_You are doing it wrong!_**

- If architecture only comes from the tests you’re asking for trouble. Just because you’re writing lots of tests it doesn’t mean your design will blossom. On the other hand, if your design sucks your tests will tell you that. They will become harder to write, too delicate to maintain, too complex to comprehend. Time to step back, think, sketch a bit and go for a refactoring rampage.
- Time spent on learning about architecture and design will pay back. To observe emerging design you need to be sensitive to a good design. Those design patterns can be useful here. But don’t over-engineer. Don’t pull in a big architecture from day one. Just let the tests guide you and surprising things will happen.

# A little detour on mocks and the price of fame

For many, using mocks has become synonymous with Test-Driven Development. I’ve even seen job ads where a candidate was required to demonstrate her fluency of TDD using mock frameworks. Perhaps the popularity comes from the fact that the style is easier to start with: you don’t have to build up the context that much, layers are easier to work on, there’s less team contention, and plenty of mock libraries available to use. While the idea of mock objects is great, it’s a tool much prone to misuse. Many accusations come to the London School of TDD of being heavily mock driven and having a bad influence on system design. This couldn’t be farther from the truth. The London school embraces the benefits of mocking while defining the best practices so the application won’t suffer from over-mocking. When committing to mocks it’s worth keeping in mind a few key points:

# ==The heavily mocked test is not its final state

==Use mocks for discovery, for deferring writing all the prod code in one go. Once you’ve got it all sorted, review if mocks are still serving the purpose, or just tying your tests to the implementation. Some mocks will be useful, get rid of the rest.

# Use mocks for awkward collaboration

Test doubles are invaluable to remove slowness or non-determinism when talking to external services, file system, or database. Mocks provide the edge you need for your tests to be fast and stable. You should also consider using fakes (objects with working but simplified implementations) which can bring similar benefits, but also be reused. Fakes are especially useful in happy-path scenarios.

# Use mocks to induce errors

Application complexity arises the moment when it needs to handle errors arising from external interactions. How to make your application resilient? Test for errors. There are many ways to induce errors in tests, mocks being one of the prominent examples.

# Only mock types that you own

Don’t mock external, third-party code. It’s a risky business to imitate intricacies of external API which you don’t fully understand. It gives you a false sense of confidence and makes your test setup harder. Introduce an adapter layer. You can reuse it all across your app without leaking external API details. When mocking adapter, you’re in control — you know the contract. Moreover, you can assess the correctness of adapter implementation with an integration test.

# Use the right mocking tool

Go and find the right tools for a job. Don’t take it for granted. Play with a few before you settle on one. If it’s hard to work with or there’s too much to remember about, go and try another one. The most popular don’t need to be the best. If your language has first-class, succinct lambda support, and it’s easy to redefine a function or a method then consider not using a mocking library. Embrace the functional programming style. In my many years with Scala and Clojure I have never had to pull in an external mocking tool.

# Summary

![](https://miro.medium.com/v2/resize:fit:496/1*4iYJmMxwRQrxoL2OChMEuA.jpeg)

I hope you had a chance to grasp the differences between the Detroit and the London Schools of TDD. By now you should understand the differences of using one style or another, their distinct take on unit testing, approach to test writing and test doubles. I hope you can see how both styles are equally useful, and not necessarily contradict each other. Which approach would you go with in the next project? Perhaps a combination of techniques can bring benefits? Choose whatever works for you. Be pragmatic, stay open-minded. As long as you test on the right level, wisely use proper tools for the job, and let your ideas materialise cleanly and consistently, you should be good. If something doesn’t work, listen to your tests and refactor. Keep your tests fast, easy to read, cheap to change. Your test harness is the living documentation of your system. It gives you confidence. It lets you sleep better at night. Praise your tests. If they don’t give you the courage to move forward… **_you’re doing it wrong_.**