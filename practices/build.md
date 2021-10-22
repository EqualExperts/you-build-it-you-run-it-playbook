# Build

These practices design and build operability into digital services. Building a digital service that is easy to operate in production creates new sources of adaptive capacity, which can be utilised in abnormal operating conditions. You might not need to implement all of these, but without a majority of them you’ll suffer from the [excessive BAU pitfall](). 

![](../.gitbook/assets/practices/build-practices.png)

**Figure 8 - build practices**

## Upskill application support analysts as product team developers

Coming soon

## Architect for adaptability

Coming soon

## Be prepared to deploy at any time

Coming soon

## Automate a telemetry toolchain

Coming soon

## Maximise discoverability of teams and services

Coming soon

|Securing You Build It You Run It in retail|
|---|
|We worked in a large merchandise retailer, building an encryption service to protect sensitive data. This included personal data, database encryption keys, and mobile payment keys. We chose to implement You Build It You Run It because the pressure to keep our services available was very high, and our infrastructure was complex. It would have been difficult to pass our services over to a separate operations team.<br><br>We made the alert system for this infrastructure quite sensitive, so we could catch all sorts of problems. However, it didn’t have the desired effect. Some alerts were too sensitive due to brief vendor instabilities, which we couldn’t fix during callouts. It decreased our attentiveness to alerts to some extent, and tired out the team. After that we concluded don’t get any alerts you can’t do anything about.<br><br>We made the decision to move to service level objectives (SLOs) for our alerts. This benefited the team a lot, as clear availability targets and priorities reduced unnecessary stress.<br><br>Our alerts were also a great tool to improve our services. As we were investigating alerts, we were often able to quickly fix the underlying problems. We then realised we should extend these practices to disaster recovery, which was a great tool for bringing the whole team up to the same level of understanding.<br><br>From this experience, I learnt that You Build It You Run It practices are worth investing in, as it is easier to react to a problem when you are woken up at night if you’ve practiced common failure patterns. When our team had new team members, we were always eager to bring them up to speed by putting them on-call.<br><br>![Natalia Oskasina](../.gitbook/assets/practices/natalia-oskasina.jpg)<br><br>[Natalia Oskasina](https://www.linkedin.com/in/natalia-oskina/)<br>Developer<br>EE UK|