# IVR Phone Tree: IVR for beginners. Powered by Twilio - ASP.NET MVC

[![Build status](https://ci.appveyor.com/api/projects/status/ktdh5pqmkc39ljng?svg=true)](https://ci.appveyor.com/project/TwilioDevEd/ivr-phone-tree-csharp)

An example application implementing an automated phone line using Twilio.

[Read the full tutorial here](https://www.twilio.com/docs/tutorials/walkthrough/ivr-phone-tree/csharp/mvc)!

## Local development

This project is built using the [ASP.NET MVC](http://www.asp.net/mvc) web framework.

1. First clone this repository and `cd` into its directory:
   ```
   git clone git@github.com:TwilioDevEd/ivr-phone-tree-csharp.git
   cd ivr-phone-tree-csharp
   ```

1. Build the solution

1. Expose your application to the wider internet using [ngrok](http://ngrok.com). This step
  is important because the application won't work as expected if you run it through
  localhost.

  To start using `ngrok` in our project you'll have execute to the following line in the _command prompt_.

  ```
  ngrok http 55585 -host-header="localhost:55585"
  ```

  Keep in mind that our endpoint is:

  ```
  http://<your-ngrok-subdomain>.ngrok.io/Conference/ConnectClient
  ```

  Remember to update the Local.config file with the generated <your-ngrok-subdomain>.

1. Configure Twilio to call your webhooks

  You will also need to configure Twilio to call your application when calls are
  received in your [*Twilio Number*](https://www.twilio.com/user/account/messaging/phone-numbers).
  The voice url should look something like this:

  ```
  http://<your-ngrok-subdomain>.ngrok.io/Conference/ConnectClient
  ```

  ![Configure Voice](http://howtodocs.s3.amazonaws.com/twilio-number-config-all-med.gif)

That's it!

## Meta

* No warranty expressed or implied. Software is as is. Diggity.
* [MIT License](http://www.opensource.org/licenses/mit-license.html)
* Lovingly crafted by Twilio Developer Education.
