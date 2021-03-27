# We're hiring! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're constanly hiring Software Engineers familiar with the Apache Kafka ecosystem (developers & ops), who know how to code on the JVM (Kotlin/Scala, a bit of Java), with a interest for smart UI/UX. Find your position here: https://www.conduktor.io/jobs/

# Challenges

## 1/ Software Development

Write a [tornadofx](https://github.com/edvin/tornadofx) application in Kotlin or a [scalafx](https://www.scalafx.org/) application in Scala (with ZIO), (or a web front-end / Scala backend but that's not how Conduktor is made yet!) where we can see records from a topic:

### I should be able to
- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck
- stop the consumption, select another topic, then consume it etc.

### Tech orientation

- Do not use Maven
- JavaFX: Do not use FXML but plain code for views.
- Kafka: Do not use consumer groups but custom partition assignments only

### How long?

Time estimated: it depends on you!

## 2/ Code Comments

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/code-comments) and tell us what do you think of them.

# Additional libraries you can use

Here are additional stuff we are using in Conduktor (Kotlin, and some Scala):

- Use [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- Use [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- Use [Arrow kt](https://arrow-kt.io/) (core & fx) to work with more functional programming data structures (Either, Validated, traverse, simili for-comprehension etc.)

If you're using Scala, you can use [ZIO](https://zio.dev/).

