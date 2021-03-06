## We're hiring! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're constanly hiring Software Engineers familiar with the Apache Kafka ecosystem (developers & ops), who know how to code on the JVM (Kotlin/Scala, a bit of Java). Find your position here: https://www.conduktor.io/jobs/

## Coding Challenge

### Software Development

Write a [tornadofx](https://github.com/edvin/tornadofx) application in Kotlin or a [scalafx](https://www.scalafx.org/) application in Scala, where we can see records from a topic:

- I should be able to set a Kafka bootstrap address
- I should be able to add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- I should be able to view all the topics
- I should be able to select a topic and consume its data from the beginning
- The application should not rely on consumer group but on custom partition assignment
- I should be able to see the records flowing without the UI to be stuck
- I should be able to stop the consumption, select another topic, then consume it etc.

Time estimated: it depends on you!

### Code Comments

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/code-comments) and tell us what do you think of them.

### Extra

Here are additional stuff we are using in Conduktor (Kotlin, and some Scala):

- Use [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- Use [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- Use [Arrow kt](https://arrow-kt.io/) (core & fx) to work with more functional programming data structures (Either, Validated, traverse, simili for-comprehension etc.)

If you're using Scala, you can use [ZIO](https://zio.dev/).

