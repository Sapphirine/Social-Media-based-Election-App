# Social-Media-based-Election-App

Team members: Ling Liu, Boya Hao

###Overview
In this project, we explored insights embedded in social media data such as tweets regarding the two currently most promising candidates Hillary Clinton and Donald Trump.
In detail, we build a realtime web application which visualizes the social media data in various ways. 
We also trained a deep-learning model using LSTM for sentiment analysis based on the self collected and labelled tweets.

###How to run:

You need to have an AWS account in order to run the Meteor since we are using AWS services such as AWS ElasticSearch and etc. You need to store your AWS credentials under the default path `~/.aws/crendentials`. You also need to create relevant ElasticSearch indices under your ElasticSearch domain created on AWS. Beside, you would need obtain API keys from IBM Alchemy and Twit as well as install Node.js and Meteor.js.

To run the web application, just go to the folder "Web" and start the meteor application

`cd yourPathName/Web`

`meteor`

You will see the web app runing at `http://localhost:3000`

To start real-time streaming of the data, type the below commands in two windows, before start the stream, make sure you install all the packages in the package.json by `npm install`

Window 1:
`cd yourPathName/Collection\ and\ Processing/TweetMap`
`node tweetmapserver.js`

Window 2:
`cd yourPathName/Citizen\ and\ Processing/Citizen\ Reaction`
`node tweetserver.js`
`node aggregator.js`


