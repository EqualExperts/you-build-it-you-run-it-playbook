# Operational Enablers

These practices allow on-call product teams to collaborate effectively with operational enabler teams. This includes:

* Integrating digital services into service management processes for change management, incident management, and more.
* Working with specialist teams such as database administrators and network administrators.

You Build It You Run It co-exists with Ops Run It, as a hybrid operating model. Product teams use the same workflows that operations teams use for COTS and foundational systems. This helps operations teams to buy into product teams managing their own digital services, and it drives consistent behaviours across your organisation.

Product teams have the incentives and technical skills to automate integration touchpoints. They collaborate with operational enabler teams to implement fully automated workflow schemes for digital services. Over time, COTS and foundational systems can be migrated to the same workflow schemes, and everyone benefits from faster, more reliable service management. 

![](../.gitbook/assets/practices/operational-enabler-practices.png)

**Figure 9 - operational enabler practices**

These practices are based on our principle of [operating models are selected on financial exposure and product feature demand](https://you-build-it-you-run-it.playbook.ee/principles#operating-models-are-selected-on-financial-exposure-and-product-feature-demand). If you’re unable to establish them, you’ll suffer from the [Operations treacle pitfall](https://you-build-it-you-run-it.playbook.ee/pitfalls#operations-treacle).

## Pre-approve low risk, repeatable changes

Establish pre-approved change requests for low risk and repeatable changes. Continue to use change approvals for high risk and/or unrepeatable changes. In ITIL v3, this is the difference between standard changes and normal changes. This ensures regular, automated production deployments performed by an on-call product team can happen in a timely fashion. 

Integrate into these change management actions:

* Allow a product manager to create a pre-approved change request template for a digital service.
* Automatically raise a change request when the last pre-production activity is successfully completed:
    * For a low risk and repeatable change, complete a pre-approved change request.
    * For a high risk or unrepeatable change, send a change request to a change manager for approval. 
* Automatically check prior to a production deployment that an approved change request exists, and do not permit a deployment if none is found.
* Automatically close the change request when the production deployment is completed.

This facilitates a high proportion of low risk changes for a digital service, and a regular cadence of successful production deployments. 

## Integrate into incident management as is

Coming soon

![](../.gitbook/assets/practices/integrating-into-incident-management-as-is.png)

**Figure 10 - integrating into incident management as is**

Coming soon

## Implement compliance as code

Coming soon

## Establish specialists as a service

Coming soon

![](../.gitbook/assets/practices/dba-specialists-as-a-service.png)

**Figure 11 - DBA specialists as a service**

Coming soon

|The support toolchain for You Build It You Run It at a payments provider|
|---|
|We were engaged by one of the leading EMEA payments providers to build a payment gateway which could be white labelled for each tenant. The payments gateway was launched in multiple countries, with different payment integrations for different tenants.<br><br>The product team responsible for building the payments gateway was also responsible for running on-call support. Understanding the product features helped us to surface and monitor the right metrics. We also built an extensible alerting system, which could be configured for each tenant. When a new tenant was onboarded, a default alerting profile was assigned to them. The alerting profile was then gradually updated, based on the transaction volume and payment features opted into by the tenant. This helped to avoid false alerts.<br><br>Since the same team was responsible for building and running the payments gateway, we iterated on metrics and alerts as part of every feature cycle. We ensured every request was traced across services and external integrations. Dashboards were built for every alert, to reduce the response time for them. When the alerts were triggered, the product team was notified along with the right dashboards. Being on-call gave us an accurate context to prioritise and fix errors as they occurred.<br><br>![Anant Pal](../.gitbook/assets/practices/anant-pal.jpg)<br><br>[Anant Pal](https://www.linkedin.com/in/anantkpal/)<br>Anant Pal<br>EE India|