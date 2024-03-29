# We're hiring a QA Engineers! 👨‍💻 👩‍💻

We're hiring QA Engineers experimented with TypeScript to help us make amazing products.

## 1. The Application Process

Please read this if you want to apply: [How our Application process works?](../application-process.md). This is necessary to ensure your application process will be smooth.

## 2. The Challenge

You'll write some e2e tests for [AKHQ](https://akhq.io/), a tool similar to our product.

To run AKHQ locally on your computer, we're providing you two scripts, [start_akhq.sh](start_akhq.sh) and [stop_akhq.sh](stop_akhq.sh).    
You'll need to have installed [Docker](https://www.docker.com/products/docker-desktop/) first on your computer to run these scripts.

To start AKHQ,
- clone this repository on your computer
- in a terminal, go into the `qa-engineers` directory
- run `./start_akhq.sh`
- wait for a few seconds (it can be slow) 
- in your browser, go to `localhost:8080`.    
  You should see something like this: 

![](akhq_welcome_page.png)

We ask you to write 3 e2e tests for AKHQ.

### Constraints

1. You must write your tests with TypeScript and [Playwright](https://www.playwright.dev/).
2. Your tests must be run on Chrome, Safari and Firefox.
3. Your code must be committed to a private repository on GitHub.     
4. Your code must contain a `README.md` file explaining how to run the tests and anything you think is important for us to know.

### Test 1 - Show hidden topics

On the "Topics" page, when the user selects "Show all topics" in the dropdown list present in the filters of the table and then clicks on the "Search" button, 
the table should at least show 2 additional lines.     
One of the additional lines must contain `__consumer_offsets` as the Topic name.    
The other additional line must contain `_schemas` as the Topic name.    

### Test 2 - Create a topic

From the "Topics" page, the user can create a new Topic via the "Create a topic" button.     
Write a test suite validating that creating a Topic works in AKHQ.    

### Test 3 - Live Tail

AKHQ is a nice interface on top of [Apache Kafka](https://kafka.apache.org/).

Apache Kafka is a kind of letter box where some programs will publish some messages into (it's called "producing"), and some other programs will wait for and read these messages when they arrive (it's called "consuming").     
Once a message is produced, the programs waiting for it will receive it and do something with it.     

Messages are sent in things called "topics" so that some programs can consume from some topics while some other programs will consume from some other topics.

AKHQ has a "Live Tail" feature that allows you to consume from a Topic in live.    
You tell AKHQ which Topic to consume from, and it'll start to wait for messages produced to that Topic.    
Once a message is produced in that Topic, AKHQ will show it in the UI.    

We ask you to write a test suite proving that the Live Tail feature works.    
Your test must:
- create a new Topic
- start the Live Tail on this new Topic
- produce a message in that Topic 
- validate that the message you produced has been displayed by the Live Tail you started previously    

### (Optional) Going further

This part of the exercise is optional.

Configure Github Actions to run your tests automatically.

### Once done

Email us to tell us that you're done.

Have fun 🚀