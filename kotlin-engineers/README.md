# We're hiring Kotlin/Kafka Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Software Engineers familiar with the Apache Kafka ecosystem (as Developers & Ops) and Kotlin.

- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.

## Business requirements: a mini-Conduktor

Write an application that displays records flowing in *real-time* from a topic.

For this challenge, write a Rich Application in Kotlin with 2 modules:
- `ui`: [tornadofx](https://github.com/edvin/tornadofx), it is using JavaFX behind the scene
- `kafka`: to deal with Apache Kafka (connection, list topics, consume records...)

### I should be able to

- set a Kafka bootstrap address, and be able to set additional properties (security etc.)
- list the topics
- select a topic and consume its data from the beginning
- see the records flowing without the UI to be stuck in real-time

### Technical requirements

- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)
- Use gradle, no Maven
- Use JDK 11+ or more. (you may use the branch `jdk10` of tornadofx if you're using it)
- JavaFX: Do NOT use FXML but plain code for views.

### Inspiration

Don't hesitate to download and run our product to see this in action: https://www.conduktor.io/

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)

### If you use Kotlin, consider using...

- [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html): equivalent of supervised Fibers in ZIO
- [Flow](https://kotlinlang.org/docs/reference/coroutines/flow.html): equivalent of ZStream
- [Arrow](https://arrow-kt.io/): Either, Validated, traverse, etc.