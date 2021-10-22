# Build

These practices design and build operability into digital services. Building a digital service that is easy to operate in production creates new sources of adaptive capacity, which can be utilised in abnormal operating conditions. You might not need to implement all of these, but without a majority of them you’ll suffer from the [excessive BAU pitfall](https://you-build-it-you-run-it.playbook.ee/pitfalls#excessive-bau). 

![](../.gitbook/assets/practices/build-practices.png)

**Figure 8 - build practices**

These practices link back to our principle of [operating models are most effective when rapid restoration comes first](These practices link back to our principle of operating models are effective when rapid restoration comes first. ). 

## Upskill application support analysts as product team developers

If you’re transitioning your digital services from Ops Run It, invest in your application support analysts and help them become product developers.  

You Build It You Run It is all about incorporating operational knowledge into the design of digital services, and application support analysts are an invaluable source of such knowledge. They have a deep appreciation of operating conditions, live traffic management, and historical incidents. Upskilling analysts allows them to contribute their institutional knowledge to building operability into digital services. For example, ex-analysts with prior on-call experience can teach other product team developers how to refine alerts and minimise unnecessary callouts. 

Upskilling analysts is a significant investment. We recommend creating opportunities for motivated, skilled employees interested in new career pathways. We'd adopt a gradual pace using learning materials and pair-programming, to minimise disruption for your product teams and operations teams alike. 

You Build It You Run It creates new opportunities for your application support analysts. They can remain in an operations team committed to COTS and foundational systems, and increase their technical mastery. Alternatively, they can join a product team dedicated to a digital service, and learn how to use software delivery skills to solve business problems. Some of the best product team developers we've worked with have a background in Ops Run It. 

## Architect for adaptability

Design loosely-coupled product teams and loosely-coupled digital services, to enable graceful degradation when a production failure inevitably occurs. This allows customers to partially use your digital services, and your business outcomes to be partially realised, while full availability is restored in the background. 

Architecting for adaptability also protects an on-call product team from [excessive BAU](https://you-build-it-you-run-it.playbook.ee/pitfalls#excessive-bau). Minimising service dependencies and the blast radius of anticipated failures allows a product team to prioritise availability protection over planned feature development, because there’s a high standard of service reliability, which results in a low level of BAU work. 

This is deeply contextual, and it varies from one digital service to another. For example, a digital service could comprise a modular monolith of many business functions, or multiple microservices per business function. Empower product teams to make their own choices, reduce failure blast radius, and remove inter-team overheads in deployment orchestration and/or incident response wherever possible. 

Architecting for adaptability takes many forms:

* *Eliminate avoidable service dependencies*. Draw the bounded context of a digital service to ensure minimal dependencies on other digital services and third party systems. 
* *Soften unavoidable service dependencies*. Ensure communications with downstream digital services and third party systems are via asynchronous queues, bulkheads, circuit breakers, on the wire caches, and rate limiters wherever appropriate. 
* *Create availability redundancy*. Leverage cloud infrastructure to establish multi-zone availability for digital service workloads, followed by multi-region availability if necessary. 
* *Set up single team ownership for digital services*. Design product and technology boundaries so one on-call product team has exclusive write access to the code repositories, configuration, and more for a digital service. One team can own multiple digital services, but a digital service can only have one owning team.
* *Establish single service ownership for databases*. Create database infrastructure so one digital service has exclusive read and write access to a relational or non-relational database. A digital service can use multiple databases, but a database instance can only have one digital service consumer. 
* *Share behaviours via APIs not closed-source libraries*. Prevent the use of closed-source code libraries by mandating open-source code libraries for infrastructure code reuse, and digital services for business logic reuse. See [Don't share libraries among microservices](https://blog.philipphauer.de/dont-share-libraries-among-microservices/) by Philip Hauer.
* *Shutter a service on failure*. Create user-friendly shutter pages to replace API and frontend entry points for a digital service for when it is entirely unavailable.
* *Shift some incident resolution onto customers*. Experiment with self-service fix actions and chatbots to introduce L0 customer support. We see this infrequently, when on-call costs have been incurred in a repeatable failure scenario that cannot easily be eliminated. 

Pressure to create faster, better, cheaper digital services actively undermines efforts to increase organisational resilience. It’s important to always consider long-term extensibility alongside short-term gains. See [An interview with David Woods](https://increment.com/reliability/resilience-engineering-david-woods/) by Ipsita Agarwal.

## Be prepared to deploy at any time

Ensure a digital service is always deployable. This means a monolith or a set of microservices are always passing their automated functional tests, always ready to be signed off in exploratory testing, and always prepared to go through a deployment process into production. This includes:

* *XP development practices*. Gradually introduce pair-programming, test-driven development, Trunk Based Development, and Continuous Integration into product teams.
* *Deployment pipelines*. Create fully automated deployment pipelines for all activities between code commit and production deployment.   
* *Parallelised functional tests*. Use dynamic test data and prime test runners to run suites of functional tests in parallel.
* *Zero downtime deployments*. Establish blue-green deployments, canary deployments, and/or dark launching to put new product features in front of customers in the day time,  without any availability loss.  
* *Fast revert on failure*. Allow a failed build, test suite, or deployment to be immediately reverted within seconds of failure detection.  

The ability to deploy at any time enables a rapid incident response. As usual, we recommend a product team experiments with different approaches until the right fit is found. It’s possible you won’t need all of these in your organisation.

## Automate a telemetry toolchain

Coming soon

## Maximise discoverability of teams and services

Coming soon

|Securing You Build It You Run It in retail|
|---|
|We worked in a large merchandise retailer, building an encryption service to protect sensitive data. This included personal data, database encryption keys, and mobile payment keys. We chose to implement You Build It You Run It because the pressure to keep our services available was very high, and our infrastructure was complex. It would have been difficult to pass our services over to a separate operations team.<br><br>We made the alert system for this infrastructure quite sensitive, so we could catch all sorts of problems. However, it didn’t have the desired effect. Some alerts were too sensitive due to brief vendor instabilities, which we couldn’t fix during callouts. It decreased our attentiveness to alerts to some extent, and tired out the team. After that we concluded don’t get any alerts you can’t do anything about.<br><br>We made the decision to move to service level objectives (SLOs) for our alerts. This benefited the team a lot, as clear availability targets and priorities reduced unnecessary stress.<br><br>Our alerts were also a great tool to improve our services. As we were investigating alerts, we were often able to quickly fix the underlying problems. We then realised we should extend these practices to disaster recovery, which was a great tool for bringing the whole team up to the same level of understanding.<br><br>From this experience, I learnt that You Build It You Run It practices are worth investing in, as it is easier to react to a problem when you are woken up at night if you’ve practiced common failure patterns. When our team had new team members, we were always eager to bring them up to speed by putting them on-call.<br><br>![Natalia Oskasina](../.gitbook/assets/practices/natalia-oskasina.jpg)<br><br>[Natalia Oskasina](https://www.linkedin.com/in/natalia-oskina/)<br>Developer<br>EE UK|