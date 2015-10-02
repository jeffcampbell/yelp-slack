# yelp-slack
Get Yelp search results in Slack

![example image](http://i.imgur.com/jet2aBz.png)

### What you will need
* A [Heroku](http://www.heroku.com) account
* A [Yelp](https://www.yelp.com/) account
* An [outgoing webhook token](https://api.slack.com/outgoing-webhooks) for your Slack team

### Setup
* Clone this repository locally
* Create a new Heroku app and follow the instructions to initialize the ```yelp-slack``` repository
* Use the [Yelp API](https://www.yelp.com/developers/documentation/v2/overview) page to generate API credentials 
* Navigate to the settings page of the Heroku app and add the following config variables:
  * ```OUTGOING_WEBHOOK_TOKEN``` The token for your outgoing webhook integration in Slack (more on this in a bit)
  * ```BOT_USERNAME``` The name the bot will use when posting to Slack
  * ```BOT_ICON``` The emoji icon for the bot
  * ```YELP_CONSUMER_KEY``` The consumer key for your Yelp API credentials
  * ```YELP_CONSUMER_SECRET``` The consumer secret for your Yelp API credentials
  * ```YELP_TOKEN``` The token for your Yelp API credentials
  * ```YELP_TOKEN_SECRET``` The token secret for your Yelp API credentials
  * ```RADIUS``` The radius for the search in meteres. Maximum radius is 40000 meters (25 miles)
  * ```LOCATION``` The center of the radius for your searches. Can be a zip code, neighborhood, adress, or city
* Navigate to the integrations page for your Slack team. Create an outgoing webhook, choose a trigger word (ex: ".lunch"), use the URL for your heroku app, and copy the webhook token to your ```OUTGOING_WEBHOOK_TOKEN``` config variable.
* Push the repository to the Heroku app
* Try a search (ex: ".lunch pizza"). You should get a recommendation back.

### Thanks
[Yelp Ruby Gem](https://github.com/Yelp/yelp-ruby)

[@gesteves](https://github.com/gesteves/) Who's code I am constantly referencing.
