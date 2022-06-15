# We're hiring Senior Scala/Kafka Software Engineers! 👨‍💻 👩‍💻

Don't hesitate to do the challenges presented here and tell us: jobs@conduktor.io!

We're hiring Senior/Mid Software Engineers familiar with the Apache Kafka ecosystem (as Developers & Ops) and Scala/ZIO.

- Job description to read: [Software Engineers](https://jobs.lever.co/conduktor/cd77a517-cb07-4f1c-8ec4-ec5b16d33f11).
- Please read this if you want to apply: [How our Application process works?](../application-process.md). This is
  necessary to ensure your application process will be smooth.

# The Challenge

Conduktor is a software company centered around Apache Kafka.

You are a Senior Software Engineer at Conduktor.     
Because you're a Senior, you were proposed to, and you accepted to, start the development of a new product.     
This product will start only with you as engineer but your team will gradually grow to 6+ backend engineers once you've
implemented the initial/minimal codebase.     
This product will live and grow for years. It's the new big product the company is investing in.     
This product is not an experimentation. It's not a POC.     
The company has already conducted experiments that led to the conclusion that this product will be a huge success.    
The POC of this product is already selling very well but is buggy because developed extremely quickly, to test the
market fit of the idea.

The tech stack of the other products of the company is:

- Scala
- ZIO
- Caliban
- sbt
- Github and Github Actions

The minimum things that your project must provide before the company starts to give you more engineers is a private
API (it'll only be used by a FE in React developed internally) allowing the client to:

- Connect to an Apache Kafka cluster
- List its topics with metadata
- Consume records from its topics in *real-time*
  - Consider adding an initial option, like a filter, a "start from" option, or a "limit" option.

Initially and until the team get to a certain size, you'll be the only Senior engineer technically leading the project.    
The company will provide you mid and junior engineers to help you with the development.    
You'll need to onboard them efficiently because you'll also have a lot of dev work yourself.     
To not lose too much time onboarding them, write a document explaining the software architecture of the project so that
they can just read it to get up to speed with the code and architecture.     
Please add anything you think is important to the document regarding your project, so that any engineer joining your project can understand the
practices of your team, what is expected from them and so can quickly start to produce relevant PRs to your project.     

### Technical requirements

- Use a private Github repository
- Apache Kafka: Do NOT use consumer groups but custom partition assignments (no group id should be used)

### How long?

Time estimated: it depends on you!

It's really the "job" at Conduktor, just think that it's your onboarding. :-)
