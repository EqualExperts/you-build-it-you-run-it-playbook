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

Unplanned operational work doesn't count towards planned product or operational features. We've heard this expressed as "BAU work”. Day to day operational tasks simply need to be completed by a product team, and they constitute rework. If the amount of BAU work is excessive, a product team cannot complete planned work when expected by the product manager.

This pitfall happens when digital services cannot gracefully degrade on failure, when production deployments aren't consistently applied in all environments, and when the telemetry toolchain isn't fully automated. Excessive BAU can be hard to detect, because product teams don't always track operational rework in a ticketing system like Jira. Product team members might fix intermittent alerts, deployment failures, infrastructure errors etc. without a ticket. It can be spotted by measuring the percentage of time product team members spend on planned work, each week.

To avoid this pitfall:

* [Treat unplanned operational rework like planned work](https://you-build-it-you-run-it.playbook.ee/practices/build#treat-unplanned-operational-rework-like-planned-work), so operational rework can be tracked and managed like any planned work
* [Re-architect digital services for adaptability](https://you-build-it-you-run-it.playbook.ee/practices/build#architect-for-adaptability), so graceful degradation on failure is possible
* [Create a fully automated deployment pipeline](https://you-build-it-you-run-it.playbook.ee/practices/build#be-prepared-to-deploy-at-any-time), so failed deployments are minimised and can be quickly reverted
* [Establish an automated telemetry toolchain](https://you-build-it-you-run-it.playbook.ee/practices/build#automate-a-telemetry-toolchain), so dashboards and alerts are reliable and can be updated at any time

We don't see this pitfall in practice as often as it's feared. We believe the fear of it comes from the historic levels of operational rework incurred for on-premise software services. For cloud-based digital services, a lot of operational changes are automatically handled by the cloud provider.

## Change management treacle

Coming soon

## No major incident management

Coming soon

## Not enough embedded specialists

Coming soon

## Limited on-call schedule

Coming soon

|Lost sponsor in retail|
|---|
|Coming soon<br><br>![Julia Wilson](../.gitbook/assets/practices/julia-wilson.jpg)<br><br>[Julia Wilson](https://www.linkedin.com/in/julia-l-wilson/)<br>Developer<br>EE UK|