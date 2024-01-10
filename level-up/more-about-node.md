# ![Intro to Node - Level Up - More About Node](./assets/hero.png)

**Learning Objective:** By the end of this lesson students will be able to explain why Node.js is an in demand skill for modern developers. 

## Enthusiasm for Node.js

Node.js has garnered significant enthusiasm and adoption in the tech industry. Let's explore the reasons behind this trend.

### High performance

- **Increased Efficiency**: One of the primary reasons for Node.js's popularity is its high performance. Businesses can handle more traffic with less hardware, resulting in cost savings and improved scalability.

### Developer flexibility

- **JavaScript Everywhere**: Node.js allows developers to use JavaScript on both the client and server sides. This flexibility makes it easier for developers to work across the full stack, streamlining development processes.
- **Developer Utilization**: Companies benefit from this by having a more flexible and efficient developer workforce, capable of handling both front-end and back-end development.

### Business implications

- **Cost Savings**: The combination of server performance and developer efficiency translates into significant cost savings for businesses.
- **Wide Adoption**: This economic advantage has led to widespread adoption of Node.js across various industries.

![Node users from different industries](assets/originals/node-users.png)

*Image Source: [RisingStack Blog](https://blog.risingstack.com/what-is-node-js-used-for-2017-survey/)*

### Demand for Node developers

- **Career Opportunities**: The broad adoption of Node.js has created a solid demand for skilled Node.js developers in the job market.

## Node.js and performance

To understand why Node.js is highly performant, it's essential to recognize the impact of Input/Output operations.



**Latency Impact**: Input/Output type operations, especially network requests, can be time-consuming and are often the bottleneck in web applications.

![Latency numbers every programmer should know](assets/originals/latency-numbers.png)

tktk hunter -- not sure where this is originally from, but another option is to remake if you think it adds value

*Image illustrates the relative latencies of various operations.*

### Asynchronous and event-driven architecture

- Node.js uses an asynchronous and event-driven design. This means that I/O operations do not block the execution of other tasks in the application.

- As a result, a Node.js server can efficiently support a large number of concurrent connections without significant performance degradation.

> 📚 *Asynchronous, Event-Driven Design*: This programming paradigm allows tasks to be executed concurrently and independently, improving the responsiveness and throughput of applications, especially in network-intensive scenarios.
