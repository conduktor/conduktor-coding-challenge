# We're hiring Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Software Engineers familiar with the Apache Kafka ecosystem (as Developers & Ops) and the JVM (Kotlin/Scala/ZIO), with an interest for smart UI/UX.

# 1. The Job requirements

Please confirm that you fit our position: [Software Engineers](https://apply.workable.com/conduktor/j/A7E3C47339/).

# 2. The Application Process

Please read this if you want to apply: [How our Application process works?](../application-process.md).

This is necessary to ensure your application process will be smooth.

# 3. The Challenge

## Build a mini-Conduktor

Write an application that displays records flowing in *real-time* from a topic.

> Today, Conduktor is a heavy-weight client—in Kotlin/Scala without HTTP API. We ask you to follow the same pattern for this challenge because this is the current implementation. We have planned to move to a React-based application + Scala API but we're not there yet. Still, if you know React, you can also write a Front-end + a Scala API (http4s/ZIO) instead of using JavaFX.

- a module for the UI: in Kotlin or Scala
  - Use [tornadofx](https://github.com/edvin/tornadofx) (Kotlin) OR [scalafx](https://www.scalafx.org/) (Scala)
- a Scala/ZIO module to deal with Apache Kafka (connect, list topics, consume records...)

If you're using Kotlin for the view, you must deal with the interop ZIO <-> Coroutine and ZStreams <-> Flow.

### I should be able to

- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck
- stop the consumption, select another topic, then consume it etc.

### Tech orientation

- Do not use Maven, only sbt or gradle
- Use JDK 11+ or more. (no JDK 8) (you may use the branch `jdk10` of tornadofx if you're using it)
- JavaFX: Do NOT use FXML but plain code for views.
- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

## Comment the code

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/software-engineers/code-comments) and tell us what do you think of them.

# If you use Kotlin

Here are additional stuff you should be using with Kotlin:

- [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html): don't use basic `Thread`s to do async stuff. Coroutine are like Fibers, can scale massively without impact and provide automatic supervision (parent-child relationships). This is idiomatic in Kotlin.
- [Flow](https://kotlinlang.org/docs/reference/coroutines/flow.html): equivalent of RxJava, Reactor, Akka Streams, ZIO Streams etc. in Kotlin
- [Arrow](https://arrow-kt.io/): the Functional companion to Kotlin's Standard Library (Either, Validated, traverse, etc.)


