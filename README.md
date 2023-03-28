# ⚠️ This repository is no longer maintained.

<img src="https://developer.nexmo.com/assets/images/Vonage_Nexmo.svg" height="48px" alt="Nexmo is now known as Vonage" />

## Support Notice
This is an archived repository. If you have any questions, feel free to reach out to us at devrel@vonage.com or through our Community Slack at https://developer.vonage.com/community/slack.

<hr />

This repository is part of the [How to Send SMS Messages With Java](https://learn.vonage.com/blog/2017/05/03/send-sms-messages-with-java-dr/) tutorial.

### Prerequisites

* [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html)
* [Gradle](https://gradle.org/) for building your project
* A [Vonage Account](https://dashboard.nexmo.com/) and [Virtual Number](https://dashboard.nexmo.com/buy-numbers)

*We've built this example using JDK 16 and Gradle 7.1*

## Running Instructions
Navigate to the project folder in your terminal and run:

```shell
gradle build
```

In `SendSMS.java`, replace the placeholders with string values as follows:

| KEY                 | DESCRIPTION                                                                                                              |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------|
| `VONAGE_API_KEY`    | Your API key, shown in your [account overview](https://dashboard.nexmo.com/).                                            |
| `VONAGE_API_SECRET` | Your API secret, shown in your [account overview](https://dashboard.nexmo.com/).                                         |
| `TO_NUMBER`         | The number you are sending the SMS to in [E.164 format](https://en.wikipedia.org/wiki/E.164). For example 447401234567.  |
| `VONAGE_BRAND_NAME` | Sender ID, the number or text shown on a handset when it displays your message.                                          |

> Note: In some countries (US), `VONAGE_BRAND_NAME` has to be one of your Vonage virtual numbers. In other countries (UK), you're free to pick an alphanumeric string value—for example, your brand name like AcmeInc. Read about country-specific SMS features on the [dev portal](https://developer.vonage.com/messaging/sms/guides/country-specific-features).


Save and run `gradle run`. 

You should see something like this printed to the screen:  

`Message sent successfully.[com.vonage.client.sms.SmsSubmissionResponseMessage@f0f0675[to=447401234567,id=13000001CA6CCC59,status=OK,remainingBalance=27.16903818,messagePrice=0.03330000,network=23420,errorText=<null>,clientRef=<null>]]`

... and you should receive a text message! If it didn't work, check out if something was printed after `ERR:` in the line above, and maybe wait a few more seconds for the message to appear.

### References
* Go to the [tutorial](https://learn.vonage.com/blog/2017/05/03/send-sms-messages-with-java-dr/)
* [Vonage SMS API Reference](https://developer.vonage.com/api/sms?theme=dark)
* [Vonage Java SDK](https://github.com/Vonage/vonage-java-sdk)
* [Country Specific SMS Features](https://developer.vonage.com/messaging/sms/guides/country-specific-features)
