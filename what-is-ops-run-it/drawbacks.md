# Drawbacks of Ops Run It

Ops Run It has a lot of drawbacks for digital services. They're systemic, and not the fault of any delivery or operations team. They're generally related to the [hard divide between siloed delivery and operations teams](https://you-build-it-you-run-it.playbooks.ee/what-is-ops-run-it). Countermeasures are sometimes available, albeit with their own costs and complexity.

Ops Run It creates a [diffusion of responsibility](https://en.wikipedia.org/wiki/Diffusion_of_responsibility). Product managers are responsible for launching products they don't support, and are incentivised to prioritise product features over operational features. Delivery teams are responsible for building services they don't support, and are incentivised to maximise deployments. Operations teams are responsible for supporting services they don't build, and are incentivised to minimise deployments. This results in a slow time to market, reliability problems, and/or limited learning opportunities.  

Due to these drawbacks, Ops Run It can't sustain weekly or more frequent deployments. There's an underinvestment in operability, and a burden on the operations teams grows as the number of delivery teams increases. Eventually, they become a significant organisational bottleneck, through no fault of their own. 

## Deployment throughput 

* *Slow change approvals*. Change requests take hours, days, or weeks to be signed off. In fact, Dr. Forsgren *et al* demonstrated in [*Accelerate*](https://www.amazon.co.uk/Accelerate-Software-Performing-Technology-Organizations/dp/1942788339) that not having a change approval process leads to more positive outcomes than an ITIL change process. 
  * A change management team can be slow to pick up a change request, if they have one queue for all incoming work and/or it's an ITIL normal change request with a 3-5 day response time.
  * A change management team can be slow to approve a change request, if a CAB meeting requires a business justification, rollback plan, etc. from the delivery team.  
  * Slow deployments. Deployments take hours or days to complete successfully. 
  * An application support team can be slow to take on a deployment, if they have one queue for all incoming work and their own operational work to prioritise. 
  * An application support team can have to contend with a semi-automated deployment process, intermittent failures, and ambiguous documentation from delivery teams.
  * An application support team can be unable to create an automated deployment pipeline, if ownership of the deployment process is shared with delivery teams.
* *Zero focus on outcomes*. Digital services are created as outputs with no regard for customer outcomes. Delivery teams lack the access to live traffic data necessary to form product hypotheses. 
* *High knowledge synchronisation costs*. Knowledge synchronisation takes hours or days between operations and delivery teams. An application support team can require knowledge transfer meetings and/or runbook updates for every deployment. 
* *Scheduling conflicts*. Deployments are rescheduled on short notice. An application support team suffers from management escalations and fluctuating priorities, as delivery team stakeholders seek faster results for themselves. 
* *Contractual deployment charges*. Traditional supplier contracts discourage an increase in deployments. An outsourced application support team can charge a lower rate for two or three deployments per month, a higher rate for rollbacks, and a much higher rate for more frequent deployments.

These drawbacks add up to high opportunity costs, with potential revenue lost due to the long lead times to launch new product features. The obvious countermeasure is to create a fully automated deployment pipeline, to reduce errors and speed up the deployment process. We'd strongly recommend a deployment pipeline, and caution that it can't tackle most of these drawbacks alone. For example, it can't eliminate the delays incurred on each handoff between teams.  

## Service reliability

## Reactive culture