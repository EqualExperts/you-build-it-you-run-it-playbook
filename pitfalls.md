# Pitfalls

Below are the pitfalls we've encountered when implementing [You Build It You Run It](https://you-build-it-you-run-it.playbook.ee/what-is-you-build-it-you-run-it). Each pitfall drains confidence in the operating model, and ultimately puts it in jeopardy. 

It's particularly important to guard against these pitfalls if your organisation previously migrated away from [Ops Run It](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it). A predisposition to central operations teams may still exist in your organisation. If one or more pitfalls have a negative impact, your senior leadership may see a return to Ops Run It as a quick, cost efficient way to safeguard the reliability of digital services.

## Linear run costs

This looks like: 

* *Run cost directly linked to product team count*. Your product teams each have a product team member on-call out of hours, and each one impacts on-call funding.

This pitfall happens when you have an on-call standby cost model of $*R*(*n*), where *R* is the remuneration rate per person and *n* is the number of teams on-call. As you increase your number of product teams, your on-call standby costs increase in kind. 1 team costs $*R*(*1*), 10 teams costs $*R*(*10*), and 20 teams costs $*R*(*20*).

A linear run cost can't happen with Ops Run It. One app support analyst on-call for all your foundational systems produces a cost model is $*R*(*1*). In addition, the remuneration rate per person *R* can be lower, if your app support team is outsourced. 

On-call standby costs are a key operating model cost, and a linear run cost creates a perception that You Build It You Run It is too expensive. If you also suffer from the [Operations manager still accountable pitfall](https://you-build-it-you-run-it.playbook.ee/pitfalls#operations-manager-still-accountable), on-call funding is a line item in a strained opex budget and it shows linear growth.

You Build It You Run It has a [risk of high run costs](https://you-build-it-you-run-it.playbook.ee/what-is-you-build-it-you-run-it/drawbacks#service-reliability), but it's not inevitable. Furthermore, run cost alone is a flawed comparison of You Build It You Run It and Ops Run It. Operating models are [different insurance policies for different business outcomes](https://you-build-it-you-run-it.playbook.ee/principles#operating-models-are-insurance-for-business-outcomes), and their costs are multi-faceted. The [high opportunity costs](https://you-build-it-you-run-it.playbook.ee/introduction#what-is-in-this-playbook) of Ops Run It are unacceptable for digital services.

To avoid this pitfall:

1. [Select availability targets on financial exposure](https://you-build-it-you-run-it.playbook.ee/practices/selection#select-an-availability-target-on-financial-exposure), so each product team balances availability with engineering effort
1. [Select out of hours schedules on financial exposure](https://you-build-it-you-run-it.playbook.ee/practices/scale#select-out-of-hours-on-call-on-financial-exposure), so product teams at scale do not produce linear run costs

## Operations manager still accountable

This looks like:

* *Inflated availability targets*. Your product managers are tempted to select the maximum availability target and highest on-call level. 
* *Low priority operational features*. Your product managers have little reason to prioritise operational features alongside product features.
* *Weak operability incentives*. Your product teams have low motivation to constantly build operability into digital services.
* *On-call funding pressure*. Your operations manager comes under pressure to cut corners on on-call spend, whenever their opex funding is scrutinised.

This pitfall happens because your senior operations manager is still accountable for the reliability of digital services. Your product teams may feel some responsibility for their digital services, but they are not held accountable by senior leadership for production incidents. In addition, their on-call funding comes from an opex budget owned by the operations manager. 

Keeping accountability away from product teams dilutes operability incentives all round. Product managers select whatever availability target they want, because someone else is paying their on-call costs. Product teams cut corners on designing for adaptive capacity, because they won't be questioned about inoperability later on.

To avoid this pitfall:

1. [Make product team budget holders accountable for business outcomes](https://you-build-it-you-run-it.playbook.ee/practices/governance#make-product-team-budget-holders-accountable-for-business-outcomes), so product teams have sole accountability for their digital services
2. [Fund on-call costs from product team budgets](https://you-build-it-you-run-it.playbook.ee/practices/governance#fund-on-call-costs-from-product-team-budgets), so product teams have to fund on-call themselves

The impact of this pitfall can be lessened if the operations manager is supportive of You Build It You Run It, and seeks to empower on-call product teams at every opportunity. 

## Excessive BAU

This looks like:

* *Slow delivery of planned work*. Your product teams don't deliver in a timely fashion the product and operational features prioritised by product managers.
* *High number of callouts*. Your product teams spend most of their time fighting operational problems e.g. intermittent alerts, deployment failures, infrastructure errors.

Unplanned operational work doesn't count towards planned product or operational features. We've heard this expressed as "BAU work". Day to day operational tasks simply need to be completed by a product team, and they constitute rework. If the amount of BAU work is excessive, a product team cannot complete planned work when expected by the product manager.

This pitfall happens when digital services cannot gracefully degrade on failure, when production deployments aren't consistently applied in all environments, and when the telemetry toolchain isn't fully automated. Excessive BAU can be hard to detect, because product teams don't always track operational rework in a ticketing system like Jira. Product team members might fix intermittent alerts, deployment failures, infrastructure errors etc. without a ticket. It can be spotted by measuring the percentage of time product team members spend on planned work, each week.

To avoid this pitfall:

* [Treat unplanned operational rework like planned work](https://you-build-it-you-run-it.playbook.ee/practices/build#treat-unplanned-operational-rework-like-planned-work), so operational rework can be tracked and managed like any planned work
* [Re-architect digital services for adaptability](https://you-build-it-you-run-it.playbook.ee/practices/build#architect-for-adaptability), so graceful degradation on failure is possible
* [Create a fully automated deployment pipeline](https://you-build-it-you-run-it.playbook.ee/practices/build#be-prepared-to-deploy-at-any-time), so failed deployments are minimised and can be quickly reverted
* [Establish an automated telemetry toolchain](https://you-build-it-you-run-it.playbook.ee/practices/build#automate-a-telemetry-toolchain), so dashboards and alerts are reliable and can be updated at any time

We don't see this pitfall in practice as often as it's feared. We believe the fear of it comes from the historic levels of operational rework incurred for on-premise software services. For cloud-based digital services, a lot of operational changes are automatically handled by the cloud provider.

## Change management treacle

This looks like:

* *Insufficient deployment frequency*. Your product teams can't achieve weekly deployments or more.
* *Prolonged change management process*. Your change management team insists each deployment completes a time-consuming change management process.

We refer to slow, prolonged change management processes as treacle, and they have a significant impact on deployment lead times. It naturally encourages fewer, larger deployments, which makes it harder to understand the changeset and diagnose any production problems. 

This pitfall happens when your change management process is entirely reactive, a single change category is applied to all production deployments, and each deployment requires a change approval. It creates a fraught relationship between your change management team and your product teams. 

At the same time, it's important that product teams comply with internal requirements on change management, particularly if your organisation follows IT standards such as ITIL v3. A discussion  with a change management team to streamline change approvals needs to be accompanied by a commitment to preserve change auditing.  

To avoid this pitfall:

* [Pre-approve low risk, repeatable changes](https://you-build-it-you-run-it.playbook.ee/practices/operational-enablers#pre-approve-low-risk-repeatable-changes) to accelerate a majority of deployments. 
* [Automate change auditing](https://you-build-it-you-run-it.playbook.ee/practices/operational-enablers#automate-change-auditing) for compliance with change management processes.

## No major incident management

This looks like:

* *Lack of incident response collaboration*. Your product teams don't know how to involve other product teams and/or operational enabler teams in major incidents
* *Major incident ignorance*. Your incident management team don't know when digital services are experiencing major incidents
* *No crisis communications*. Your senior leadership don't know when major incidents are creating significant financial losses/

A lack of incident management creates inconsistent behaviours and communication pathways during major incidents. It has a negative impact on resolution times and financial losses incurred, when an incident requires more than one product team to be resolved.

This pitfall happens when your incident management team is excluded from the incident response process for digital services. It means different product teams will have distinct behaviours and communication methods during production incidents. It creates an impression that product teams aren't rigorous during incident response. 

Crisis communications are particularly important during a major incident, and product teams won't know who to contact or how often to contact them with incident updates. A lack of clear, timely information to senior leadership during a major incident is an easy way to create doubts about an entire operating model. 

To avoid this pitfall:

* [Integrate into incident management as is](https://you-build-it-you-run-it.playbook.ee/practices/operational-enablers#integrate-into-incident-management-as-is), to ensure incident managers can be incident commanders for digital services as well as foundational systems.

## Not enough embedded specialists

This looks like:

* *More product teams than embedded specialists*. You want an embedded specialist in each of your *n* product teams, but you have fewer than *n* embedded specialists in place.
* *Unpredictable availability of embedded specialists*. Your product teams sometimes have to wait hours or days for specialist expertise.
* *Slow recruitment of embedded specialists. *You are always trying to hire more specialists, who are either too few or too expensive to meet your needs.  
* *Heavy workload for embedded specialists*. Your embedded specialists are each assigned to multiple product teams, and constantly endure a multi-service workload.
* *Loneliness for embedded specialists*. Your embedded specialists don't spend time working together, or learning from one another, or even talking to one another.* *

This applies to any technology specialty tied to operational work - DBAs, InfoSec analysts, network admins, operability engineers, and more. Balancing breadth of cross-functional product teams and depth of specialist expertise is hard. Developers lack the expertise to complete specialist tasks themselves. We've heard this described as "we don't want developers debugging Postgres in production", and "we don't want developers learning Terraform scripting on the job". 

This pitfall happens when you have a small, central team of specialists that can't handle demand from your growing number of product teams. The common countermeasure is to embed a specialist in each product team. However, it's hard to find multiple, affordable specialists in the marketplace, and as a result your embedded specialists each have to cover multiple product teams. The result is a large expertise bottleneck is split into multiple expertise bottlenecks. Instead of spending hours or days waiting on a central specialist team, a product team waits for hours or days for its own embedded specialist to be available. 

To avoid this pitfall:

* [Establish specialists as a service](https://you-build-it-you-run-it.playbook.ee/practices/operational-enablers#establish-specialists-as-a-service), so repeatable tasks are automated as self-service functions and specialists are freed up to offer ad hoc expertise on demand

## Limited on-call schedule

This looks like:

* Product teams have a minority of team members in out of hours on-call schedules
* Product team members participating in on-call have significant disruption to their personal lives, and are on the verge of burnout

Each product team with a limited on-call schedule has digital services at risk of lengthy incident resolution times out of hours. If product team members need time off work to cope with burnout, team morale will suffer and planned product features will take longer to complete than expected.

This pitfall happens when product team members feel unprepared for on-call support, are unhappy with their remuneration, or burn out from too much time on-call over a period of time. It's important to respect the circumstances and decisions of different product team members.

To avoid this pitfall:

1. [Prepare for on-call from day one](https://you-build-it-you-run-it.playbook.ee/practices/incident-response#prepare-for-on-call-from-day-one), so product team members are well equipped to handle out of hours production alerts.
1. [Re-architect digital services for adaptability](https://trello.com/c/nIsTYeDg/121-charles-betz-preview), so digital services don’t require substantial human intervention, and are fast to fix on failure
1. [Ensure fair remuneration for on-call developers](https://you-build-it-you-run-it.playbook.ee/practices/governance#ensure-fair-remuneration-for-on-call-developers), so product team members feel compensated for the disruption to their personal lives. 
1. [Craft a sustainable on-call schedule](https://you-build-it-you-run-it.playbook.ee/practices/incident-response#craft-a-sustainable-on-call-schedule), so no one product team member spends too much time on-call out of hours.  

This pitfall affects operations teams as well. Your app support team may have some useful organisational context and experiences to contribute.

|Lost accountability in retail|
|---|
|I worked on a team at a retail customer, building a shifts app for staff mobile devices in bricks and mortar stores. We built a cloud-based platform in Azure and the mobile app with You Build It You Run It, and the benefits were clear to our customer sponsor. We achieved a time to repair of less than 10 minutes, and we deployed on average twice a day for over six months.<br><br>Unfortunately, once the shifts app became a live service and its user base hit a critical mass, its ownership changed to a different business function within the customer organisation. Some people in this new business function was unwilling to embrace our ways of working.<br><br>An [operations manager became accountable](https://you-build-it-you-run-it.playbook.ee/pitfalls#operations-manager-still-accountable) for the reliability of our shifts app. We remained responsible for supporting the app, but we were no longer permitted to perform deployments without Change Advisory Board approval. As a result, our time to repair non-critical issues increased from 10 minutes to 1 week, of which 5 days was the governance process.<br><br>By the time I left the engagement, we were down to deploying once a fortnight. It was strange, because people celebrated how quickly we could resolve live issues, and yet they didn’t quite make the connection to how important You Build It You Run It had been.<br><br>![Julia Wilson](../.gitbook/assets/practices/julia-wilson.jpg)<br><br>[Julia Wilson](https://www.linkedin.com/in/julia-l-wilson/)<br>Developer<br>EE UK|