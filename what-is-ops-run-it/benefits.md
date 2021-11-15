# Benefits of Ops Run It

We've split Ops Run It benefits into realised versus unrealised benefits, i.e. actual versus on paper benefits. In our experience, many of the theoretical benefits of a central operations team simply don't happen for digital services. 

## Realised

These are the few benefits for digital services we expect to actually see in practice.

### Deployment throughput

We don't usually see any deployment throughput benefits. For a majority of organisations, [Ops Run It can't achieve weekly or daily deployments](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/drawbacks). Some small or medium-sized organisations may overcome this, if they implement the [Ops Run It deployment throughput variant](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/deployment-throughput) and delivery teams self-service some deployments. However, it's unusual to see that work well.

### Service reliability

We see some benefits, related to cost management and governance: 

* *Low setup costs*. Ops Run It has a [low implementation cost](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/service-reliability), as it's so well-established in the IT industry. There's plenty of training courses, online reading materials, and vendor tools that are compatible with multi-level production support.
* *Low run cost*. Ops Run It has a [low run cost](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/service-reliability). The help desk, operations bridge, and application teams can centrally manage the availability of tens of digital services, plus self-hosted COTS applications and custom integrations.
* *Run cost reduction options*. Run cost can be [lowered by outsourcing](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/service-reliability), as the general skills and technical expertise for help desk, operations bridge, and application support teams are in a worldwide abundance.
* *Straightforward governance*. Accountability, responsibilities, and visibility are all easy to understand. The senior manager in the Operations function is accountable for all aspects of reliability.

For foundational systems, these benefits can outweigh the [unrealised benefits](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/benefits#unrealised) and many [drawbacks of Ops Run It](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/drawbacks). We've seen plenty of organisations outsource one or more operations teams to a third party managed service, to minimise run costs. However, if an application support team has built up substantial domain expertise with a proven impact on incident resolution times, the case for outsourcing is not as clear cut.

### Learning culture

We seek a weak learning culture in Ops Run It, without many benefits. People can learn individually from incidents, but the opportunities for entire teams to glean new knowledge are limited. There's limited new knowledge, and people are stuck in firefighting.  

## Unrealised

These are Ops Run It benefits for digital services that are often described in theory, yet we rarely see in practice.

### Deployment throughput

* *High speed delivery teams*. Insulating delivery teams from production deployments is supposed to accelerate the speed of new product features. Instead, we see large deployments stuck in handovers between delivery and operations teams, a lot of rework when deployments fail, and little positive impact on customer outcomes.  
* *Consistent deployment process*. Using the same change management and application support teams is intended to create a consistent, well-understood process for deployments. We often see a highly variable process, which depends on personal relationships or management escalations for deployments to happen when expected.

### Service reliability

#### Availability protection

* *Informative telemetry*. An operations bridge team is theoretically able to amend logs, metrics, dashboards, and alerts over time, to increase their understanding of operating conditions. We consistently see growing telemetry datasets with a low information value.
* *Comprehensive documentation*. Operations teams are supposed to have access to accurate documentation, to help them protect service availability. We invariably find a lack of up to date documentation from delivery teams.  

#### Availability restoration

* *Fast alert acknowledgement*. Having operations bridge and application support teams always on-call is meant to minimise the time between alert and acknowledgement. We've seen organisations where it takes up to twenty minutes for an application support analyst to become aware of an alert.
* *Fast incident resolution*. Routing an operations bridge team to most incidents and a skilled application support team to the remainder is supposed to minimise the time between alert and acknowledgement. We usually see a time to resolution greater than one hour.
* *Few L2 callouts*. Using an L1 operations bridge team to restart services and follow runbooks is intended to minimise L2 callouts. We nearly always see a high percentage of alerts escalated to L2 callouts, for diagnosis and availability restoration.
* *Low incident costs*. Expecting an operations bridge team to handle most alerts creates an expectation that incident costs will be flattened. We often observe a majority of alerts escalated to the application support team, a slow time to resolve incidents, and much higher incident costs than anticipated.

We suspect these unrealised benefits are based on assumptions such as service unavailability is rare, incident count is controllable, and most issues are easily resolved. Those assumptions are entirely wrong, and it's unlikely these benefits can be achieved. See [*How complex systems fail*](https://how.complexsystems.fail/) by Dr. Richard Cook.

### Learning culture

* *Informative insights*. A root cause analysis session concentrates on a single human or technical error. We regularly observe multiple contributing factors to a production incident being silently ignored.
* *Broad insight dissemination*. A root cause analysis document is supposed to be shared throughout an organisation, so anyone can benefit from the new knowledge. We rarely see document sharing with operations teams, let alone delivery teams.  
* *Fast time to improve*. The fix actions from a root cause analysis session are intended to be implemented quickly by operations and delivery teams. We usually find large queues of fix actions that take weeks or months to be prioritised, while operations and delivery teams tackle planned work instead.

We think these unrealised benefits come from the notion that a production incident stems from a single event. Unfortunately, there's no such thing as a single root cause in modern, complex software services. These benefits could be realised if there was a concerted effort to move away from root cause analysis to insight generation, but we rarely see that happen. See [Each necessary, but only jointly sufficient](https://www.kitchensoap.com/2012/02/10/each-necessary-but-only-jointly-sufficient/) by John Allspaw.