# We're hiring Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Software Engineers familiar with the Apache Kafka ecosystem (developers & ops), who work on the JVM (Kotlin/Scala/ZIO), with an interest for smart UI/UX. More details: https://www.conduktor.io/jobs/

# The Challenge

## 1/ A mini-Conduktor

Write an application that displays records flowing from a topic I've selected.

Your project will consist in 2 sub-projects:
1/ a module for the application itself with its "view" (in Kotlin or Scala)
2/ a module for Apache Kafka interactions in Scala.

- Use sbt or gradle
- For the view, write a [tornadofx](https://github.com/edvin/tornadofx) app in Kotlin OR a [scalafx](https://www.scalafx.org/) app in Scala
- Write a Scala module using ZIO to deal with Apache Kafka (list topics, consume records...)

If you're using Kotlin for the view, you must deal with the interop ZIO <-> Coroutine and ZStreams <-> Flow (the application should display the records in *real-time*, this is important)

### I should be able to

- set a Kafka bootstrap address
- add additional properties to pass to the KafkaAdmin & KafkaConsumer (security etc.)
- view all the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck
- stop the consumption, select another topic, then consume it etc.

### Tech orientation

- Do not use Maven
- Use JVM Java 11+ or more. (no Java 8) (you may use the branch `jdk10` of tornadofx if using it)
- JavaFX: Do NOT use FXML but plain code for views.
- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

## 2/ Comment the code

Review the [code-comments](https://github.com/conduktor/conduktor-coding-challenge/tree/main/software-engineers/code-comments) and tell us what do you think of them.

# If you use Kotlin

Here are additional stuff you should be using with Kotlin (we are!):

- [coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) and not basic `Thread`s to work with async stuff. It provides a more granular level, works with Fibers, can scale massively without impact, provide automatic supervision (parent-child relationships), etc.
- [`Flow<>`](https://kotlinlang.org/docs/reference/coroutines/flow.html) to make continuous data processing easier to code (like RxJava, Reactor, Akka Streams, ZIO Streams etc.)
- [Arrow kt](https://arrow-kt.io/) to work with more functional programming data structures (Either, Validated, traverse...)


