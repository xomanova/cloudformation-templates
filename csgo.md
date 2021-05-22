# Title

csgo.yml

## Description

A CloudFormation template for deploying a Counter-Strike: Global Offensive dedicated server.

Deploys two custom game modes:\
&nbsp;&nbsp;&nbsp;&nbsp;`gamemode_knivesonly`:\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Players spawn without default primary or secondary weapons.\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Buy/Freeze time is zero\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- C4 is removed\
&nbsp;&nbsp;&nbsp;&nbsp;`gamemode_deagleonly`:\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Players spawn with default primary weapon of desert eagle.\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Buy/Freeze time is zero\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- C4 is removed


### Dependencies

* AWS Subscription
* Public hosted zone on the AWS sub
* Steam account
* Steam Game Server Login Token
* Steam API key

## Links

* [Steam API Key](https://steamcommunity.com/dev/apikey)
* [Steam Game Server Account Management](https://steamcommunity.com/dev/managegameservers)
* [Creating a stack on the AWS CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html)
* [Setting game modes in rcon](https://developer.valvesoftware.com/wiki/CSGO_Game_Mode_Commands)
* [Additional rcon commands](https://www.tobyscs.com/csgo-console-commands/)

## Server Troubleshooting

* The server will be available at `cs.<your hosted zone>`
* SSH is permitted only from the template param `MyIp`, use the key provided during creation
* The running process is `/Steam/csgo-ds/srcds_run`
* Ubuntu will download the dedicated server binaries and install them as part of the userdata
* It can take up to 40 minutes to be playable

