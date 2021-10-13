# Principles

We recommend the adoption of these operating model principles before you start to implement You Build It You Run It for your digital services. All of our [You Build It You Run It practices](https://you-build-it-you-run-it.playbook.ee/practices) tie back to these principles, which represent our thinking on how operating models succeed.

## Operating models are insurance for business outcomes

An operating model is an insurance policy. It protects the business outcomes you’re trying to achieve, in exchange for a premium. 

Different insurance policies offer different levels of protection, at different premiums. The more valuable the contents of your home, the higher the premium you pay for the right house insurance. 

Different operating models offer different levels of protection, at different premiums. The more valuable your business outcomes, the more the risk of loss, the more of a premium you pay for the right operating model. 

Business outcome protection is a mix of revenue cover and cost avoidance. The weighting of the mix varies between organisations. A private sector organisation with an ecommerce website might insure for 80% revenue cover, 20% cost avoidance. A public sector organisation with a non-transactional website might want 5% revenue cover, and 95% cost avoidance. 

## Operating models are selected on financial exposure and product feature demand

An operating model is designed to safeguard levels of financial exposure, and satisfy levels of product feature demand for business outcomes. 

You need to understand the financial exposure and product feature demand for each of your software services, and select the most appropriate operating model on a case by case basis. The same blanket operating model for all software services cannot offer cost effective insurance for multiple levels of financial exposure and product feature demand. 

Business outcomes can be expressed as opportunity costs, in terms of deployment throughput and service reliability. If they map onto significant demand for new product features, the deployment target needs to be weekly deployments or more. If they represent a substantial amount of revenue and/or costs at risk upon unavailability, the availability target needs to be 99.9% or higher. At that point, a higher premium is paid in implementation efforts, in order to minimise the opportunity costs linked to the business outcomes. 

## Operating models are most effective when rapid restoration comes first

An operating model divides service reliability into availability protection and availability restoration. Business outcome protection is far more effective when rapid availability restoration is prioritised over perfect availability protection. 

Your production environment is a complex group of different systems, services, and processes, with unpredictable interactions in unrepeatable conditions. Some failure classes are preventable, others are not, and your production environment is always vulnerable to failure. We advise our customers that being able to rapidly restore availability is more important than having fewer periods of unavailability. 

Favouring a high quality incident response over zero incidents means customers enjoy a smoother experience upon failure, and business outcomes can continue to be met under partial degradation. 

## Operating models are powered by feedback

An operating model is dependent on fast feedback loops. The tighter the feedback loops, the easier it is for people to collaborate with one another, and achieve the desired customer outcomes.

Your organisation is full of knowledge on deployment throughput, service reliability, customer needs, commercial imperatives, ways of working, production incidents, and much more. Allowing that knowledge to be siloed within different individuals and teams has an insidious impact on organisational performance. Feedback signals on customer satisfaction, product deliverables, and the actions of individuals are slower and weaker. This constantly hampers improvement efforts.

Creating feedback loops within and between teams ensures that newly acquired knowledge can be rapidly disseminated to your entire organisation. Amplifying feedback prevents the same problems from repeating themselves in different digital services, and allows people to perform their work with the cumulative knowledge of your entire organisation. This makes building and running a digital service an easy habit, rather than a laborious chore. See [Atomic Habits](https://www.amazon.com/Atomic-Habits-Proven-Build-Break/dp/0735211299) by James Clear.

|Starting You Build It You Run It too soon|
|---|
|We started to work with a major UK retailer shortly before the COVID-19 pandemic hit the UK. The company had ambitions to modernise its technology estate to offer new services to customers. We built a digital platform to scale delivery up to many teams, and implemented new digital capabilities for customers. We all saw You Build It You Run It as a key part of our technology strategy.<br><br>We publicly launched new digital services at a time when uncertainty was at its highest for society. In the early days post-launch, the retailer’s high street shops were closed, people weren’t commuting into towns, and uptake of the new services was very low. There weren’t many opportunities to learn from customers.<br><br>As a result, product teams scheduled to go on-call became demotivated. It wasn’t easy to experiment and gain insights into customer behaviours, as business was down. Some teams successfully lobbied to delay on-call support until business started to pick up again, which thankfully has happened since then.<br><br>In times of low customer uptake, we learned it’s really important to plan which experiments are most important for learning, what data is needed for those experiments, and when to pivot. It would have helped us to understand how to differentiate between different levels of on-call support, and therefore the team shapes and sizes needed for You Build It You Run It.<br><br>![Ann Yong](../.gitbook/assets/principles/ann-yong.jpg)<br><br>[Ann Yong](https://www.linkedin.com/in/ann-yong-a2378724/)<br>Delivery Lead<br>EE UK|