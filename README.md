# SpeederBot
Twitter SpeederBot 

This project was setup to highlight an ongoing concern from residents with regards to excessing speeding and only intended to highlight in a visual way speeding vehicles. There is no affiliation with Here Technologies, Integromat or LivingStreets however if you are using this for profit then please consider donating at least 25% of any profit to LivingStreets to help make roads safer see links below.

You will need to setup 3 accounts one with Here Technology to get access to the Traffic Flow Data and the Second with Integromat to run the workflow (Bot) and the third a Twitter account to tweet to.

* STEP 1 -
The Bot uses a flow bounding box as the source of it's traffic flow data, draw a box around your road, test and note the 4 coordinates. https://developer.here.com/documentation/examples/rest/traffic/traffic-flow-bounding-box
Click into the "bbox" and move the map location to your desired road, try and make this as small as possible to only capture local traffic flows. Then click "Send Request" the results will appear in the black box and note down the 4 coordinates.

* STEP 2 -
Create a developer account https://developer.here.com/sign-up?create=Freemium-Basic&keepState=true&step=account then create an API Key and note it down.

* STEP 3 -
Create an account https://www.integromat.com/ (*Integromat will require Payment to run the bot*)

* STEP 4 -
Download the Scenario BluePrint from this repository (*We are asking Integromat if they will create a template to make this easier*)

* STEP 5 -
Create a new Twitter Scenario and then Import the Blueprint

* STEP 6 -
Configure the HTTP connection replacing the 4 coordinates and API with your own.

* STEP 7 -
Configure the Twitter Connector and tweet message - please keep #SpeederBot

* STEP 8 - 
Set the time schedule and activate (recommend between 10-15min) 

* STEP 9 - 
If this has been useful please consider donating towards the running of BerkshireCar [![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/P5P32P98C)

###### Notes
* It only samples data every few minutes and sometimes no traffic will be detected especally if the road is not busy.
* It will not capture all speeding vechicals and is only intended as a sample of data.
* There is a cost to running this on Integromat which is charged by the number of opperations performed.

###### Reference Links
* LivingStreets Donation Page: https://www.livingstreets.org.uk/donate
* Donations to Support BerkshireCar SpeederBot: https://ko-fi.com/berkshirecar 
* What are Traffic APIs: https://mobility.here.com/learn/travel-apis/traffic-apis-5-powerful-options-supercharge-your-application
