# Operational Enablers

These practices allow on-call product teams to collaborate effectively with operational enabler teams. This includes:

* Integrating digital services into service management processes for change management, incident management, and more.
* Working with specialist teams such as database administrators and network administrators.

You Build It You Run It co-exists with Ops Run It, as a hybrid operating model. Product teams use the same workflows that operations teams use for COTS and foundational systems. This helps operations teams to buy into product teams managing their own digital services, and it drives consistent behaviours across your organisation.

Product teams have the incentives and technical skills to automate integration touchpoints. They collaborate with operational enabler teams to implement fully automated workflow schemes for digital services. Over time, COTS and foundational systems can be migrated to the same workflow schemes, and everyone benefits from faster, more reliable service management.

![](../.gitbook/assets/practices/operational-enabler-practices.png)

These practices are based on our principle of [operating models are selected on financial exposure and product feature demand](../principles.md#operating-models-are-selected-on-financial-exposure-and-product-feature-demand).

## Pre-approve low risk, repeatable changes

Establish pre-approved change requests for low risk and repeatable changes. Continue to use change approvals for high risk and/or unrepeatable changes. In ITIL v3, this is the difference between standard changes and normal changes. This ensures regular, automated production deployments performed by an on-call product team can happen in a timely fashion.

Integrate into these change management actions:

* Allow a product manager to create a pre-approved change request template for a digital service.
* Automatically raise a change request when the last pre-production activity is successfully completed:
  * For a low risk and repeatable change, complete a pre-approved change request.
  * For a high risk or unrepeatable change, send a change request to a change manager for approval.
* Automatically check prior to a production deployment that an approved change request exists, and do not permit a deployment if none is found.
* Automatically close the change request when the production deployment is completed.

This facilitates a high proportion of low risk changes for a digital service, and a regular cadence of successful production deployments. Without it, you'll suffer from the [Change management treacle pitfall](../pitfalls.md#change-management-treacle).

## Integrate into incident management as is

Automate incident management touchpoints into your ticketing system. This allows an on-call product team to manage their own incidents with minimal friction, and demonstrates a long-term commitment to collaborating with major incident managers.

Integrate into these incident management actions:

* Notify an on-call product team member when an alert is fired.
* Create an incident in the ticketing system when an alert is fired.
* Acknowledge an incident in the ticketing system when an on-call product developer is available.
* Reassign an incident to a different digital service, COTS application, or foundational system when necessary.
* Notify an incident manager when an incident is declared as a major incident.
* Update an incident in the ticketing system when in-progress notes are available.
* Resolve an incident in the ticketing system when an alert is resolved.

We recommend paying for a SaaS incident response platform such as [PagerDuty](http://www.pagerduty.com/) or [VictorOps](http://www.victorops.com). An incident response platform orchestrates alert notifications for on-call product teams, which means an on-call product developer can be notified of an alert in under a minute. It can manage an out of hours schedule for incident managers as well as product teams, which means an on-call developer can quickly contact someone for advice during a major incident. It can also offer bi-directional updates between its own alerts and incidents in your ticketing system. This removes hours of manual efforts on tickets, and ensures high quality records are preserved.

![](../.gitbook/assets/practices/integrating-into-incident-management-as-is.png)

An incident manager could declare a major incident in the event of:

* A period of extreme unavailability e.g. the loss of [AWS US East 1](https://aws.amazon.com/message/12721/)
* A zero day security vulnerability e.g. the [Log4Shell](https://www.kaspersky.com/blog/log4shell-critical-vulnerability-in-apache-log4j/43124/) vulnerability

The incident manager creates a major incident via the incident response toolchain, which automatically contacts all on-call product teams. If the incident starts outside working hours, the incident manager uses the [information portal](./) and [service runbooks](incident-response.md#prepare-for-on-call-from-day-one) to phone any teams who lack an out of hours on-call schedule in the incident response platform. The incident manager announces themselves as incident commander, and uses an incident channel in the collaboration to work effectively with all affected product teams on the incident response.

It takes time to integrate You Build It You Run It into the same incident management process as Ops Run It, and we’ve seen it pay off multiple times. We’ve witnessed dramatic reductions in time to acknowledge and time to resolve an incident, and improvements in ways of working between different teams. If you don’t do this, you’ll fall into the [No major incident management pitfall](../pitfalls.md#no-major-incident-management).

It takes time to integrate You Build It You Run It into the same incident management process as Ops Run It, and we've seen it pay off multiple times. We've witnessed dramatic reductions in time to acknowledge and time to resolve an incident, and improvements in ways of working between different teams. If you don't do this, you'll fall into the No major incident management pitfall.

## Automate change auditing

Build each deployment pipeline as a fully automated compliance tool for change management. Accelerate change feedback loops from weeks or months into minutes.

Use a version control system such as [GitHub](https://github.com/) to store all updates to:

* Alert definitions
* Code
* Configuration
* Infrastructure definitions
* Logging dashboards
* Monitoring dashboards
* Reference data

Audit in every deployment pipeline:

* The versions of your digital services currently deployed in which environments
* The updates in your version control system that can be traced back from different versions of your digital services
* The deployment timestamps, deployer names, and approved change requests for production deployments
* The deployment lead time and deployment frequency for production deployments

This is one way to implement compliance as code. Work with your change managers to understand the reports they need to satisfy internal compliance requirements. Free them up to tackle higher value work, such as orchestrating production deployments of foundational systems. Without this, you'll suffer from the Change management treacle pitfall.

## Establish specialists as a service

Turn the skill sets of specialised operations teams into consumable services. This creates a balance between breadth of cross-functional product teams and depth of specialist expertise in operational areas.

Some operations teams possess scarce and highly valued engineering capabilities. The usual example we see is a few database administrators managing an on-premise relational database, for multiple product teams operating digital services in a cloud provider. The answer isn't to cross-train developers, or hire more database administrators. It's to eliminate repeatable work by migrating databases into your cloud provider, and by creating self-service deployment pipelines for your product teams.

Offloading and automating database tasks frees up your database administrators to provide high value expertise on demand, such as troubleshooting live performance problems. For more on this, see [Stop trying to embed specialists in every product team](https://www.equalexperts.com/blog/our-thinking/stop-trying-to-embed-specialists-in-every-product-team-2/) by Bethan Timmins.

![](../.gitbook/assets/practices/dba-specialists-as-a-service.png)

If you don't implement specialists as a service, you'll suffer from the embedded specialists pitfall, and endure time-consuming interactions with some operational teams.

| Launching a new sales platform with ITIL standard changes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>I worked in a large media company, and we were building a multi-channel sales platform. The company had a centralised change management process based on ITIL, and it wasn't suited to our aims of frequent self-managed releases.<br><br>When we started to use change requests, we found out we could use standard changes, because we had fully automated deployments and platform releases were always toggled off on deployment. We met the criteria for repeatable, low risk changes.<br><br>We then proceeded to deploy hundreds of changes to the emerging new platform under the standard change process, until we had enough functionality in production that we could turn the sales platform on. This involved some business readiness work, working closely with contact centre staff so they use the sales platform as part of the assisted sales channel. It didn't require any change approvals either.<br><br>Some months later, I bumped into a change manager, and they asked when we were going live. I advised we'd been live for months, and had hundreds of users all very happy with the new sales platform. The change manager advised standard changes didn't sound appropriate for future deployments now it was a live system, and I said we'd been continuing to deploy multiple times a week to deliver bug fixes and new features!<br><br>When I look back on that experience, I see it was my first true experience of You Build It You Run It and all the benefits. We worked closely with the product manager, with few handoffs. We had very high levels of test automation, automated deployment pipelines, and many feature flags. And all because we were responsible for our sales platform, and took that responsibility seriously.<br><br><img src="../.gitbook/assets/practices/paul-timmins.jpg" alt="Paul Timmins"><br><br><a href="https://www.linkedin.com/in/paul-timmins-89a0854/">Paul Timmins</a><br>Lead Consultant<br>EE Australia &#x26; New Zealand</p> |
