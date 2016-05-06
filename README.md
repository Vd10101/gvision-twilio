# gvision-twilio
## Google Vision API through MMS

Trying to reproduce this article: 
* [Exploring the world on-the-go using Google Cloud Vision and Twilio](http://www.blog.juliaferraioli.com/2016/02/exploring-world-using-vision-twilio.html)
* *"Let people text an image, and receive a reply with few things that the API detects in it"*
* Code available in github [here](https://github.com/juliaferraioli/cloud-vision/tree/master/python/twilio-labels)

## Prerequisites

1. Create a project in the [Google Cloud Platform Console](https://console.cloud.google.com).

2. [Enable billing](https://console.cloud.google.com/project/_/settings) for your project.

3. Enable the Vision APIs.

4. Install the [Google Cloud SDK](https://cloud.google.com/sdk)

       	$ curl https://sdk.cloud.google.com | bash
        $ gcloud init

5. Create and set up a [Twilio account](https://www.twilio.com/try-twilio) and number capable of sending and receiving MMS (make sure to whitelist your number with Twilio).

6. Install the python requirements found in `requirements.txt`

		$ pip install -r requirements.txt

## Test *What's That?!*

1. Run the sample
		
		$ python whats_that.py

2. Text an image to your Twilio number

3. See the response!

## Clean-up

1. Stop the server (`ctrl-c` or `kill` the process)

2. Delete images from Twilio [using the API](https://www.twilio.com/help/faq/sms/how-do-i-delete-messages-message-media-or-message-bodies); you can write a script to do this
 
