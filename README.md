# We're hiring! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're constanly hiring Software Engineers familiar with the Apache Kafka ecosystem (developers & ops), who know how to code on the JVM (Kotlin/Scala, a bit of Java), with a interest for smart UI/UX. Find your position here: https://www.conduktor.io/jobs/

> **We are not looking for Data Engineers or Devops, but Software Engineers only.**

# Challenges

## 1/ A mini-Conduktor

Write an application that displays records flowing from a topic I've selected. This will consist in 2 parts: a view in Kotlin and a module in Scala

- Use sbt or gradle
- Write a [tornadofx](https://github.com/edvin/tornadofx) application in Kotlin OR a [scalafx](https://www.scalafx.org/)
- Write a Scala+ZIO module to deal with the features (Apache Kafka list topics, consume records...)
- Start the application that will use the module (with interop ZIO <-> Coroutine and ZStreams <-> Flow if you're using Kotlin)

### I should be able to

- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck
- stop the consumption, select another topic, then consume it etc.

### Tech orientation

- Do not use Maven
- Use Java 11+ or more. (no Java 8) (you may use the branch `jdk10` of tornadofx if using it)
- JavaFX: Do not use FXML but plain code for views.
- Apache Kafka: Do not use consumer groups but custom partition assignments (no group id should be used)

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

## 2/ Comment the code

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/code-comments) and tell us what do you think of them.

# If you use Kotlin

Here are additional stuff we are using with Kotlin:

- Use [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- Use [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- You can use [Arrow kt](https://arrow-kt.io/) (core & fx) to work with more functional programming data structures (Either, Validated, traverse, simili for-comprehension etc.)


