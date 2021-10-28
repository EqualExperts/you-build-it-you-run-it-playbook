# Drawbacks of You Build It You Run It

## Deployment throughput

* *High setup cost*. It takes weeks or months to establish a new, streamlined change management process for digital services.
  * Moving accountability for change approvals from a change management team to product managers takes weeks or months. 
  * Moving accountability for production deployments from an application support team to on-call product teams takes weeks or months.
  * Creating a new change approval process in a central ticketing system like ServiceNow takes weeks or months. 

The countermeasure here is for product teams to solve problems for the change management team, not just for themselves. This can include providing change managers with: 

* A list of change approval criteria that product managers will consistently follow.
* A set of automated integrations for change requests into the central workflow system. 
* A standing invite to all product planning meetings and pre-deployment product demos.
* An automated email notification whenever a deployment has happened.
* An automated web page showing recent change requests and the associated deployments.

## Service reliability

* *High setup cost*. It takes weeks or months to establish incident management for digital services.
  * Moving accountability for incident management from an application support team to on-call product teams takes weeks or months. 
  * Creating a new incident management process in a central workflow system like FreshService takes weeks or months. 
  * Procuring licenses for an incident response platform such as PagerDuty takes weeks, and can become expensive at scale. 
  * Enabling production access rights for telemetry tools, deployment servers, and incident management for on-call product teams takes weeks.
  * Establishing out of hours schedules and operational training for on-call product teams takes weeks. 
* *Risk of high run cost*. Remuneration for multiple product team developers on call for multiple digital services can be higher than a single application support team analyst on call for all digital services.

In our experience, organisations underestimate the high setup cost and overestimate the risk of a high run cost with You Build It You Run It. The setup cost can be reduced by collaborating with your incident management team on:

* An incident management process that on-call product teams will consistently follow.
* A set of automated integrations for incidents into the central workflow system.
* A standing invite to all product planning meetings and Chaos Days.
* A per-team license setup for telemetry tools and incident response tools, where possible.

## Learning culture

* *High setup cost*. It takes weeks or months to create a new incident review process for digital services.
  * Moving accountability for problem management from an application support team to on-call product teams takes weeks.
  * Setting up cross-team knowledge sharing after post-incident reviews takes weeks.  
  * Incident analysis training for on-call product teams takes weeks or months. 
  * Establishing psychological safety within on-call product teams for post-incident reviews takes weeks or months.
  * Creating a blameless culture between on-call product teams takes weeks or months.

There aren't any obvious countermeasures here. An upfront investment in effective incident analysis training is vital, as moving away from root cause analysis is a subtle paradigm shift. It's an entirely different way of understanding organisational problems, and it takes time to build up momentum for continuous improvement. 

|You Build It You Run It skepticism in financial services| 
|---|
|I worked with a large financial services company that wanted to use modern techniques and tools to revamp its digital offering. The existing digital product was run on-prem using Ops Run It, and it had plenty of problems.<br><br>For example, when a public-facing service was slow to respond to customer interactions, the development team was asked why, and their response was “we'll ask the Ops team”. They had no knowledge of how the product performed in the customers' hands, and didn't have the diagnostics or metrics to answer such questions.<br><br>We spun up a couple of teams, to build infrastructure and bootstrap new digital capabilities. We brought forward new ideas that represented a 180 degree turn for the company. These included using cloud infrastructure, building a digital platform, moving to Continuous Delivery, and adopting You Build It You Run It. Each of them took months to be signed off.<br><br>Things slowly took a turn for the better. Cloud became a first-class citizen in the fabric of the organisation. Delivery teams were given operational control of the services they built, and our platform team gave them early access to observability and operational tooling. As a result, we saw an increase in deployment frequency, and operational engagement from the developers.<br><br>Although the company made a lot of progress, there were still plenty of caveats. The need for regular penetration exercises delayed deployments, and a preference for out of hours deployments was hard to shake off. Still, I could see how You Build It You Run It had started to shape a financial services company into a software delivery powerhouse.<br><br>![](../.gitbook/assets/what-is-you-build-it-you-run-it/charles-tumwebaze.png)<br><br>[Charles Tumwebaze](https://www.linkedin.com/in/charles-tumwebaze-a4361847/)<br>Lead Developer<br>EE South Africa|