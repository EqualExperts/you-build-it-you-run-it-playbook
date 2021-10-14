# Selection

These practices refer to the initial selection of an operating model. We believe a hybrid operating model is essential, because we agree with Martin Fowler’s statement that a software service is either a [strategic differentiator or a utility](https://martinfowler.com/bliki/UtilityVsStrategicDichotomy.html). We consider a digital service to be a strategic differentiator, and a foundational system to be a utility. 

Our operating model selector is below. Once you understand your failure tolerances and different levels of feature demand, you can map out which operating model is right for you. 

![](../.gitbook/assets/practices/operating-model-selector.png)

**Figure 2: operating model selector**

To help understand which operating model is best for your software service, you can follow these selection practices. 

![](../.gitbook/assets/practices/selection-practices.png)

**Figure 2: selection practices**

These practices are linked to our principles of operating models are [insurance for business outcomes](https://you-build-it-you-run-it.playbook.ee/principles#operating-models-are-insurance-for-business-outcomes), and [operating models are selected on financial exposure and product feature demand](https://you-build-it-you-run-it.playbook.ee/principles#operating-models-are-selected-on-financial-exposure-and-product-feature-demand).

## Select an availability target on financial exposure

Coming soon

## Select deployment target on feature demand

Coming soon

## Select a higher availability target for peak exposure

Coming soon

## Select You Build It You Run It for 99.99% availability

Coming soon

## Select You Build It You Run It for digital services

Coming soon

## Select Ops Run It for foundational systems

Coming soon

|Traffic lights You Build It You Run It in retail|
|---|
|I worked at a large retailer in Australia, where we gradually moved teams and their services from Ops Run It to You Build It You Run It. The transition can be hard, and to ensure a pragmatic approach we introduced a traffic light system. We used it to help us decide if a service should remain in Ops Run It, or be moved to You Build It You Run It.<br><br>We tracked outcomes for each service, including its availability target and deployment frequency target, to determine where they were on the traffic lights.<ul><li>Red was for a fortnightly deployment target, or lower and meant Ops Run It.</li><li>Green was for a weekly deployment target or higher, and meant You Build It You Run It.</li><li>Amber was for a deployment target that lay in between. The service availability target was used as a tiebreaker. We had previously concluded 99.9% was not possible to achieve under Ops Run It, as it only permitted 44 minutes of downtime in a month. So a target of 99.9% or higher meant You Build It You Run It, and a target of 99.0% or lower meant Ops Run It.</li></ul>The traffic light system meant we could look at services holistically. We could build a clear picture of how many services were in Ops Run It, how many were ready to transition into You Run It, and how many required more careful thought. It allowed us to clearly see across the digital estate where we needed to focus our efforts, on changing the operational model to gain the biggest benefit to the organisation.<br><br>![Tony Nguyen](../.gitbook/assets/practices/tony-nguyen.jpg)<br><br>[Tony Nguyen](https://www.linkedin.com/in/tonynguyenoz/)<br>Director<br>EE Australia|