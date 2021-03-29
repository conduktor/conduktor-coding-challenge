# We're hiring! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're constanly hiring Software Engineers familiar with the Apache Kafka ecosystem (developers & ops), who know how to code on the JVM (Kotlin/Scala, a bit of Java), with a interest for smart UI/UX. Find your position here: https://www.conduktor.io/jobs/

> **We are not looking for Data Engineers or Devops, but Software Engineers only.**

# Challenges

## 1/ A mini-Conduktor

Write an application that displays records flowing from a topic I've selected.

- Write a [tornadofx](https://github.com/edvin/tornadofx) application in Kotlin (that's how Conduktor is made)
- OR a [scalafx](https://www.scalafx.org/) application in Scala+ZIO
- OR a web front-end / Scala+ZIO backend (that's not how Conduktor is made)

### I should be able to

- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck
- stop the consumption, select another topic, then consume it etc.

### Tech orientation

- Do not use Maven
- Use Java 11+ or more. (no Java 8)
- JavaFX: Do not use FXML but plain code for views.
- Kafka: Do not use consumer groups but custom partition assignments only
- If you're using Scala, you must also use [ZIO](https://zio.dev/).

### How long?

Time estimated: it depends on you!

## 2/ Comment the code

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/code-comments) and tell us what do you think of them.

# Additional libraries you can use in Kotlin

Here are additional stuff we are using in Conduktor (Kotlin, and some Scala):

- Use [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- Use [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- Use [Arrow kt](https://arrow-kt.io/) (core & fx) to work with more functional programming data structures (Either, Validated, traverse, simili for-comprehension etc.)



