# Incident response

These practices relate to responding to incidents, and learning from incidents. One of the drawbacks of You Build It You Run It is its [high setup cost](https://you-build-it-you-run-it.playbook.ee/what-is-ops-run-it/drawbacks), and part of that is a steep learning curve for product teams. It's important they're prepared to identify, resolve, and learn from production incidents, before their first incident occurs. If these practices aren't implemented, you'll have unprepared incident responders and they'll fall into the [excessive BAU](https://you-build-it-you-run-it.playbook.ee/pitfalls#excessive-bau) and [unsustainable on-call schedule pitfalls](https://you-build-it-you-run-it.playbook.ee/pitfalls#unsustainable-on-call-schedule). 

![](../.gitbook/assets/practices/incident-response-practices.png)

**Figure 12 - incident response practices**

These practices link back to our principle of [operating models are effective when rapid restoration comes first](https://you-build-it-you-run-it.playbook.ee/principles#operating-models-are-most-effective-when-rapid-restoration-comes-first).

## Prepare for on-call from day one

Set on-call expectations in product teams from the moment they start to build digital services. This maximises incentives for product team members to build operability into product features. It gives them time to adjust to a new mindset, in which they could be called out at 0300 to fix their own work.  

On-call preparation includes:

* *Inception*. Work with the product manager and intended users to understand the required availability level, and how best to gracefully degrade upon unavailability. See our [Inception Playbook](https://inception.playbook.ee/) by Neha Datt *et al*.	
* *Runbook*. Start a runbook on day one, and update it weekly with anticipated failure scenarios, failure mitigations, alert thresholds, and step by step guides.
* *Telemetry*. Update logging dashboards, monitoring dashboards, and alert definitions for every product feature. Encourage product team members to check dashboards daily.
* *Onboarding*. Set on-call expectations with prospective team members before they join. Assign telemetry and incident response permissions to new product team members as soon as they join. 
* *Escalation path*. Ensure product team members have clear communication pathways for major incidents. Make it easy to nominate an incident manager as incident commander for out of hours incidents. 
* *Learning mindset*. Foster a no-blame culture of collaborative learning for production incidents. Promote an emphasis on creating new knowledge for the entire organisation.

These changes can be difficult to implement when you have a tight launch deadline for a new digital service. It’s important to make them a bit at a time, starting from day one.

## Craft a sustainable on-call schedule

Encourage a product team to manage an out of hours on-call schedule, which safeguards the reliability of digital services and preserves work-life balance for product team members.

We recommend:

* A minimum of three product team members participating in the on-call schedule
* All product team members are encouraged to participate in the on-call schedule, regardless of role
* A default on-call rotation of one week for each on-call participant

Some team members may be unable to do on-call for family or health reasons, and their decisions need to be respected. Some team members may be reluctant due to a lack of preparation, and any such problems need to be solved.

## Run regular Chaos Days

Inject failures into digital services to validate they have been [architected for adaptability](https://you-build-it-you-run-it.playbook.ee/practices/build#architect-for-adaptability). Enable product teams to hone their incident response skills, prior to any actual production incidents. 

Run day-long events that introduce failures into your digital services. Encourage your product teams to reduce the blast radius of latent faults, refine their mental models, and build up relationships with dependent teams. If your production environment can’t handle a controlled level of stress, run a Chaos Day in a test environment. 

To find out more about running Chaos Days in large enterprise organisations, see our [Chaos Day playbook](https://chaos-day.playbook.ee/) by Lyndsay Prewer. 


## Calculate in-incident financial losses

Coming soon

## Broadcast incident insights

Coming soon

|You Build It You Run It in PCI payments|
|---|
|Coming soon<br><br>![Raj Wilkhu](../.gitbook/assets/practices/raj-wilkhu.jpg)<br><br>[Raj Wilkhu](https://www.linkedin.com/in/rajwilkhu/)<br>Lead Developer<br>EE UK|