# Engineering coding challenge 👨‍💻 👩‍💻

Please find below instructions for our coding challenge. This is a core part of our interview process and is designed to give you insight into the real-life projects we work on here at Conduktor. 

# The Challenge

We build tools that truly unleash the power of Apache Kafka. For this challenge we would like you to build a mini-Conduktor API.  Please find our instructions and requirements below.

## Business requirements: a mini-Conduktor API

We would like you to write an API (with several endpoints) to:

- Connect to an Apache Kafka cluster
- List its topics with metadata
- Consume records from its topics in *real-time*
  - Consider adding some options like filters, start from etc.

### Technical requirements

- Use a private Github repository
- Use Scala and ZIO
- You can write a REST API or a GraphQL API, this decision is up to you
- Write tests for your API (please make it work!)
- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)
- Only sbt

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)
