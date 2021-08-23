# SpeederBot
Twitter SpeederBot 

PLEASE READ - ISSUES LOG - BEFORE IMPLEMENTING https://github.com/BerkshireCar/SpeederBot/issues

This project was setup to highlight an ongoing concern from residents with regards to excessing speeding and only intended to highlight in a public way speeding vehicles. There is no affiliation with Here Technologies, Integromat or LivingStreets however if you are using this for profit then please consider donating at least 25% of any profit to LivingStreets to help make roads safer see links below.

**Update**: The twitter blueprints are **NOT recommended** for continuous use, see issue #4 instead it's recommeded you modify them to output the results to a google sheet or airtable.

You will need to setup 3 accounts one with Here Technology to get access to the Traffic Flow Data and the Second with Integromat to run the workflow (Bot) and the third a Twitter account to tweet to.

* STEP 1 -
The Bot uses a flow bounding box as the source of it's traffic flow data, draw a box around your road, test and note the 4 coordinates. https://developer.here.com/documentation/examples/rest/traffic/traffic-flow-bounding-box
Click into the "bbox" and move the map location to your desired road, try and make this as small as possible to only capture local traffic flows. Then click "Send Request" the results will appear in the black box and note down the 4 coordinates.

* STEP 1.1 -
Check the output of the Send Request. Here Technologies appear to provide outputs for Major Trunk Roads. These are A-Roads and Motorways. Although there are some B-Roads included in the output, these appear to be the exception.

* STEP 2 -
Create a developer account https://developer.here.com/sign-up?create=Freemium-Basic&keepState=true&step=account then create a REST API Key and note it down.

* STEP 3 -
Create an account https://www.integromat.com/ (*Integromat will require Payment to run the bot*)

* STEP 4 -
Download the Scenario BluePrint from this repository (*We are asking Integromat if they will create a template to make this easier*) **NOTE**: Make sure the downloaded file is ASCII (TEXT) and has not word wraped the lines.

* STEP 5 -
Create a new Twitter Scenario and then Import the Blueprint - **NOTE** the the import option is only available with basic and above account types not the free service.

![STEP 5 1](https://user-images.githubusercontent.com/74529369/129582492-4e2a9085-f7a1-4bad-be47-da4a7feeaa26.png)  
* STEP 5.2 - click on the 3 dots at the bottom  ![STEP 5 2](https://user-images.githubusercontent.com/74529369/129582523-a56909b6-b6bf-4b0b-b358-e93c124390de.png)

* STEP 6 -
Configure the HTTP connection replacing the 4 coordinates and API with your own & replace the API key with the one your setup in STEP 2, make sure your remove the <> they are not needed.

* STEP 7 -
Configure the Twitter Connector and tweet message - please keep #SpeederBot

* STEP 7.1 - The blueprints have a filter set to MPH > 155 to enable testing before tweeting
* ![Screenshot 2021-08-18 23 58 53](https://user-images.githubusercontent.com/74529369/129982873-ed33e998-eee1-4e90-9d88-cd5d972977e6.png)

* STEP 8 - 
Set the time schedule and activate (recommend between 10-15min) 

* STEP 9 - 
If you have read all the issues in the issue log, have been using it for some time and it has been useful please consider donating towards BerkshireCar [![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/P5P32P98C)

###### Notes
* It only samples data every few minutes and sometimes no traffic will be detected especally if the road is not busy.
* It will not capture all speeding vechicals and is only intended as a sample of data.
* There is a cost to running this on Integromat which is charged by the number of opperations performed.

###### Reference Links
* LivingStreets Donation Page: https://www.livingstreets.org.uk/donate
* Donations to Support BerkshireCar SpeederBot: https://ko-fi.com/berkshirecar 
* What are Traffic APIs: https://mobility.here.com/learn/travel-apis/traffic-apis-5-powerful-options-supercharge-your-application
