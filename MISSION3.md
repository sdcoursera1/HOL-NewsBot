#Mission 3: Identifying an image using Bing Computer Vision API

Alright you're pretty much on your own for this mission. The goal of the mission is to be able to let the bot know you want to scan an image. The bot then takes in a url, sends it to Bing CV, and gets the caption.

The completed conversation if you complete this mission should look like this:

![Completed](https://raw.githubusercontent.com/alyssaong1/HOL-NUSHackathon/master/Images/Mission3/m3result.PNG)

**Note that you MUST use LUIS!**

I'm feeling generous today so here are some hints: 

- You'll need the Bing Computer Vision API. [Here's](https://dev.projectoxford.ai/docs/services/56f91f2d778daf23d8ec6739/operations/56f91f2e778daf14a499e1fe) the API reference. Refer to it when building your options for the API call in your code. Retrieving the subscription keys is similar to how you did it for LUIS and the news search. 

- The options for your API call should be in the following format:

```js
var options = {
            method: 'POST', // thie API call is a post request
            uri: '**REFER TO API REFERENCE AND FIND OUT THE API ENDPOINT**',
            headers: {
                'Ocp-Apim-Subscription-Key': '**YOUR BING CV KEY**',
                'Content-Type': '**REFER TO API REFERENCE**'
            },
            body: {
                url: '**THE IMAGE URL PROVIDED BY THE USER**'
            },
            json: true
        }
```
[Here's](https://github.com/request/request-promise) the full documentation to request-promise in case you need it. 

####If you think you got it, put https://heavyeditorial.files.wordpress.com/2016/05/harambe-22.jpg in and let us know what the caption is. No cheating! We will be reviewing your code and potentially asking questions.