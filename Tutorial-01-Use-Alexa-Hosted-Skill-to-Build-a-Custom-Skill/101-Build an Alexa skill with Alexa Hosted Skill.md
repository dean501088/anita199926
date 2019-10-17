## Getting Started with Alexa-Hosted Skill to Build an Alexa Skill

<p style="text-align:center">
<img src="./images/000-lab_architecture.png" alt="000-lab_architecture.png" width="95%">
</p>

## Overview

Alexa is the voice service that powers Echo device, or skills, that enable customers to interact
with devices in a more intuitive way using voice.
Alexa is built in the cloud, so it is always getting
smarter.

Under the trend of AIoT, Alexa is no longer just a smart speaker, and is gradually compatible with various hardware devices, such as: cars, refrigerators, etc, Which has prompted a large number of developers to devote the development of Alexa skill.

## Scenario

In this lab we will create a [Minecraft](https://www.minecraft.net/zh-hant/) helper skill for Alexa, this skill can let user to ask Alexa how to get the materials and build your tools in Minecraft without interrupt your game experience.

## Prerequisite

- Register for an [__Amazon Account__](https://www.amazon.com/ap/register?_encoding=UTF8&openid.assoc_handle=usflex&openid.claimed_id=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.identity=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.mode=checkid_setup&openid.ns=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0&openid.ns.pape=http%3A%2F%2Fspecs.openid.net%2Fextensions%2Fpape%2F1.0&openid.pape.max_auth_age=0&openid.return_to=https%3A%2F%2Fwww.amazon.com) ***(not AWS account)**


## Lab tutorial

### Sign up Amazon Developer Account with Amazon Account

If you already have an __Amazon Developer Account__, please skip this step.

- Get into [Amazon Developer Account](https://developer.amazon.com/?&sc_category=Owned&sc_channel=RD&sc_campaign=Evangelism2018&sc_publisher=github&sc_content=Content&sc_detail=howto-nodejs-V2_CLI-1&sc_funnel=Convert&sc_country=WW&sc_medium=Owned_RD_Evangelism2018_github_Content_howto-nodejs-V2_CLI-1_Convert_WW_beginnersdevs&sc_segment=beginnersdevs) catalog page.

<p style="text-align:center">
    <img src="./images/001-Alexa-Developer_console-01.jpg" alt="001-Alexa-Developer_console-01.jpg"  width="70%">
</p>

- Select __Alexa__, and you will be taken to the Amazon Alexa console.

<p style="text-align:center">
    <img src="./images/002-Alexa-Developer_console-02.jpg" alt="002-Alexa-Developer_console-02.jpg" width="70%">
</p>

- Select __Sign In__ with your __Amazon account__ on the upper right corner.

    > After sign in, you will turn back to Alexa console automatically.

- Move your mouse over the __Account Name__ on upper right corner, and select __Complete Registration__.

<p style="text-align:center">
<img src="./images/003-Alexa-Sign_up-01.jpg" alt="003-Alexa-Sign_up-01.jpg" width="70%">
</p>

<p style="text-align:center">
<img src="./images/004-Alexa-Sign_up-02.jpg" alt="004-Alexa-Sign_up-02.jpg" width="60%">
</p>

> Now we have to sign up the Amazon Developer Account step by step.

- Insure the required field has been fill in, and then select __Save and Continue__.

<p style="text-align:center">
<img src="./images/005-Alexa-Sign_up-03.jpg" alt="005-Alexa-Sign_up-03.jpg" width="70%">
</p>

<p style="text-align:center">
<img src="./images/006-Alexa-Sign_up-04.jpg" alt="006-Alexa-Sign_up-04.jpg" width="70%">
</p>

- In this step, you can just roll down and select __Accept and Continue__.

<p style="text-align:center">
<img src="./images/007-Alexa-Sign_up-05.jpg" alt="007-Alexa-Sign_up-05.jpg" width="70%">
</p>


<p style="text-align:center">
<img src="./images/008-Alexa-Sign_up-06.jpg" alt="008-Alexa-Sign_up-06.jpg" width="70%">
</p>

- Select __No__ for two option, and choose __Save and Continue__.

    > Select __No__ to save some time for the next steps. 


<p style="text-align:center">
<img src="./images/009-Alexa-Sign_up-07.jpg" alt="009-Alexa-Sign_up-07.jpg" width="70%">
</p>

- Choose __Alexa__ on the panel, and select __Alexa Skills Kit__.

<p style="text-align:center">
<img src="./images/010-Alexa-Sign_up-08.jpg" alt="010-Alexa-Sign_up-08.jpg" width="70%">
</p>

<p style="text-align:center">
    <img src="./images/011-Alexa-Create_skill-01.jpg" alt="011-Alexa-Create_skill-01.jpg" width="70%">
</p>

### Create an Custom Alexa Skill

- Select __Create Skill__ on your alexa developer console.

<p style="text-align:center">
<img src="./images/012-Alexa-Create_skill-02.jpg" alt="012-Alexa-Create_skill-02.jpg" width="80%">
</p>

- Type `yourskillname`, and choose __English__ as default language.

    >This is the name that will be shown in the Alexa Skills Store

<p style="text-align:center">
<img src="./images/013-Alexa-Create_skill-03.jpg" alt="013-Alexa-Create_skill-03.jpg" width="80%">
</p>


- Add a __Custom__ model to your skill. 


<p style="text-align:center">
<img src="./images/014-Alexa-Create_skill-04.jpg" alt="014-Alexa-Create_skill-04.jpg" width="70%">
</p>


- Choose __Alexa-Hosted__, let AWS host our backend resources.

<p style="text-align:center">
<img src="./images/015-Alexa-Create_skill-05.jpg" alt="015-Alexa-Create_skill-05.jpg" width="70%">
</p>

> With an Alexa-hosted skill, you can get started quickly using Alexa-hosted AWS resources to power your skill without leaving the console.

- Roll up the page, and select __Create skill__.

    > It will take one to three minutes to create environment.

<p style="text-align:center">
<img src="./images/016-Alexa-Create_skill-06.jpg" alt="016-Alexa-Create_skill-06.jpg" width="50%" >
</p>

- Select __Invocation__ on left side.

<p style="text-align:center">
<img src="./images/017-Alexa-Invocation_name-01.jpg" alt="017-Alexa-Invocation_name-01.jpg" width="60%">
</p>

- change __Skill Invocation Name__ to `minecraft helper`.

    > The __Skill Invocation Name__ is the key words that awake Alexa to use this skill.

<p style="text-align:center">
    <img src="./images/018-Alexa-Invocation_name-02.jpg" alt="018-Alexa-Invocation_name-02.jpg" width="70%">
</p>

- Select __Save Model__ and then __Build Model__ on the top of this field.

    > You will see a message after __Build Model__.

<p style="text-align:center">
    <img src="./images/019-Alexa-Invocation_name-03.jpg" alt="019-Alexa-Invocation_name-03.jpg" width="70%">
</p>

- Select __JSON Editor__ on your left side.

<p style="text-align:center">
<img src="./images/020-Alexa-Edit_JSON-01.jpg" alt="020-Alexa-Edit_JSON-01.jpg" width="60%">
</p>

- Download the [__module__](../Tutorial-01-Use-Alexa-Hosted-Skill-to-Build-a-Custom-Skill/module/VUI_JSON.json), and upload the __VUI_JSON.json__ file.

    > Don't forget to __Save Model__ and __Build Model__ again.
    
<p style="text-align:center">
<img src="./images/021-Alexa-Edit_JSON-02.jpg" alt="021-Alexa-Edit_JSON-02.jpg" width="70%">
</p>

> You should notice that __Intents__ and __Slot Types__ will auto populate based on the JSON Interaction Model that you have now applied to your skill. 
   
<p style="text-align:center">
<img src="./images/022-Alexa-Intent-01.jpg" alt="022-Alexa-Intent-01.jpg" width="50%">
</p>


> You can also select an intent by expanding the Intents from the left side navigation panel.


<p style="text-align:center">
<img src="./images/023-Alexa-Intent_insert-02.jpg" alt="023-Alexa-Intent_insert-02.jpg" width="70%">
</p>

> Add some more sample utterances for your newly generated intents __optionally__, but be sure to click __Save Model__ and __Build Model__ after you're done making changes here.

### Deploy the Code by Alexa-Hosted Code Editor

- Select __Code__ on upper panel.

<p style="text-align:center">
<img src="./images/024-Alexa-lambda_code-01.jpg" alt="024-Alexa-lambda_code-01.jpg" width="80%">
</p>


- If you the message on upside, select __Use Alexa hosted endpoint__.

<p style="text-align:center">
<img src="./images/025-Alexa-lambda_code-02.png" alt="025-Alexa-lambda_code-02.png" width="90%">
</p>
 

- You will see a console just like __AWS Lambda__.

<p style="text-align:center">
<img src="./images/026-Alexa-lambda_index-01.jpg" alt="026-Alexa-lambda_index-01.jpg" width="90%">
</p>


- Clean up all the original __index.js__, and copypaste the [__Index.js__](../Tutorial-01-Use-Alexa-Hosted-Skill-to-Build-a-Custom-Skill/lambda/index.js). Then, click __Save__.

- Double click the __package.json__ on left side, clean up the original content and paste the [__package.json__](../Tutorial-01-Use-Alexa-Hosted-Skill-to-Build-a-Custom-Skill/lambda/package.json) as previous step. Then, click __Save__.

- Select the __Icon__ as following to add a new file.

<p style="text-align:center">
<img src="./images/027-Alexa-lambda_file_add-01.jpg" alt="027-Alexa-lambda_file_add-01.jpg" width="50%">
</p>

- Type `lambda/recipes.js` as __File Path__, and __Create File__.

<p style="text-align:center">
<img src="./images/028-Alexa-lambda_file_add-02.jpg" alt="028-Alexa-lambda_file_add-02.jpg" width="50%">
</p>


- Copy the [__recipes.js__](../Tutorial-01-Use-Alexa-Hosted-Skill-to-Build-a-Custom-Skill/lambda/recipes.js), and paste in the __recipes.js__ file what you created.

- Select __Save__ and then __Deploy__.

    > Wait for two minutes, you will see the message

<p style="text-align:center">
<img src="./images/029-Alexa-lambda_deploy-01.jpg" alt="029-Alexa-lambda_deploy-01.jpg" width="70%">
</p>

> This will deploy your code into a Lambda function that is automatically managed for you by the Alexa-Hosted service.

### Testing Your Alexa Skill with Alexa Simulator

- Select __test__ on upper panel.

<p style="text-align:center">
<img src="./images/030-Alexa-Test_skill-01.jpg" alt="030-Alexa-Test_skill-01.jpg" width="80%">
</p>

- Extend the list, and choose __Development__.

<p style="text-align:center">
<img src="./images/031-Alexa-Test_skill-02.jpg" alt="031-Alexa-Test_skill-02.jpg" width="70%">
</p>

- Type or say `Alexa, open the minecraft helper`.

<p style="text-align:center">
<img src="./images/032-Alexa-Test_skill-03.jpg" alt="032-Alexa-Test_skill-03.jpg" width="70%">
</p>

> You will receive the response from Alexa Simulator

<p style="text-align:center">
<img src="./images/033-Alexa-Test_skill-04.jpg" alt="033-Alexa-Test_skill-04.jpg" width="90%">
</p>

- Now, you can ask everything can be created in Minecraft world, try to type `how can I get a sugar cane`.

<p style="text-align:center">
<img src="./images/036-Alexa-Test_skill-06.jpg" alt="036-Alexa-Test_skill-06.jpg" width="60%">
</p>


> NOTES : If you are idle for too long, you need to wake up "Minecraft skill" again by saying or typing "Alexa, open the minecraft helper".

<p style="text-align:center">
<img src="./images/034-Alexa-Test_skill-05.jpg" alt="034-Alexa-Test_skill-05.jpg" width="70%">
</p>

- Alexa will remember your pronunciation, and understand what you mean. 

<p style="text-align:center">
<img src="./images/035-Alexa-Test_flow-01.png" alt="035-Alexa-Test_flow-01.png" width="80%">
</p>

## Conclusion

Amazon Alexa is a big step forward when it comes to voice control
technology. It's always on microphones and integration with third-party apps means that there really are a ton of things that you can do using just your voice.
Now, you can build your custom skills if you like! 

## Reference

- [Alexa-Hosted Skill](https://developer.amazon.com/docs/hosted-skills/build-a-skill-end-to-end-using-an-alexa-hosted-skill.html)