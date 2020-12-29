## Coding Challenge

 Write a [tornadofx](https://github.com/edvin/tornadofx) application in Kotlin where we can see records from a topic:

- I should be able to set a Kafka bootstrap address
- I should be able to view all the topics
- I should be able to select a topic and consume its data
- I should be able to see the records flowing without the UI to be stuck
- I should be able to stop the consumption, select another topic, then consume it etc.

### Extra

Here are additional stuff we are using in Conduktor:

- Use [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- Use [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- Use [Arrow kt](https://arrow-kt.io/) (core & fx) to work with more functional programming data structures (Either, Validated, traverse, simili for-comprehension etc.)
