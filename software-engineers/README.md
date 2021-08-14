# We're hiring Scala/Kafka Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Software Engineers familiar with the Apache Kafka ecosystem (as Developers & Ops) and Scala/ZIO.

- Job description to read: [Software Engineers](https://apply.workable.com/conduktor/j/A7E3C47339/).
- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.

## Business requirements: a mini-Conduktor

Write an application that displays records flowing in *real-time* from a topic.

For this challenge, pick one style:

1/ A rich client (using JavaFX) composed of 2 modules (as we do today):
- ui: [tornadofx](https://github.com/edvin/tornadofx) (Kotlin) or [scalafx](https://www.scalafx.org/)
- kafka: to deal with Apache Kafka (connection, list topics, consume records...) using Scala/ZIO

2/ React + Scala API (where we are going):
- a webapp for the UI
- an API to deal with Apache Kafka (connection, list topics, consume records...) using Scala/ZIO/http4s

### I should be able to

- set a Kafka bootstrap address, and be able to set additional properties (security etc.)
- list the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck in real-time

### Technical requirements

- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)
- Only sbt or gradle, no Maven
- Use JDK 11+ or more. (you may use the branch `jdk10` of tornadofx if you're using it)
- JavaFX: Do NOT use FXML but plain code for views.

### Design Inspiration

Our existing product:

<img src="https://user-images.githubusercontent.com/3936459/129449736-1f953556-30e9-44af-b753-fab8806fde69.png" width=500 />

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

### If you use Kotlin, consider using...

- Scala/Kotlin interop to write: ZStreams -> Flow, ZIO -> Coroutine
- [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html): equivalent of supervised Fibers in ZIO
- [Flow](https://kotlinlang.org/docs/reference/coroutines/flow.html): equivalent of ZStream
- [Arrow](https://arrow-kt.io/): Either, Validated, traverse, etc.
