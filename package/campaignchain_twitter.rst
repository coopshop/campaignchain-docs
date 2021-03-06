CampaignChain Twitter
=====================

This documentation covers the standard `Twitter`_ functionality available by
default in the CampaignChain Community Edition.

Features
--------

- Connect a Twitter stream to CampaignChain with username and password
- Assign a Twitter message to a campaign
- Include up to 4 pictures in a Tweet
- Schedule a Tweet to automatically post it on Twitter at a given date and time
- Assign a responsible person to a Tweet
- Track the customer journey from an included link to the Location of a
  connected Channel (e.g. a Website page)
- Once a Tweet was posted, regularly collect statistical data about likes
  and re-tweets
- Ensure that the same Twitter content won't be posted within 24 hours to avoid
  a duplicate status message error

Packages
--------

The standard Twitter functionality is being provided by CampaignChain, Inc.
through these packages:

- `campaignchain/channel-twitter`_
- `campaignchain/location-twitter`_
- `campaignchain/activity-twitter`_
- `campaignchain/operation-twitter`_

Although these modules are based on `Symfony bundles`_, they do not work
independently of CampaignChain.

Installation
------------

The above modules are included in the Community Edition by default.

Configuration
-------------

.. _twitter-oauth-app-configuration:

Before you can post on Twitter from within CampaignChain, an OAuth app must be
created in Twitter:

#. Go to https://dev.twitter.com/apps and create a new application.
#. Fill out any required fields such as the application name and description.
#. Put your website domain in the Website field.
#. Provide the host name of your CampaignChain instance as the Callback URL
   (e.g. http://mydomain.com). Make sure that you specify the correct scheme
   (`http` or `https`). If you omitted the Callback URL, the app won't work with
   CampaignChain.
#. The Callback URL's parts must be identical with the
   `router.request_context.host` and `router.request_context.scheme` parameters
   defined in the `app/config/parameters.yml` configuration file.
#. Once you have registered the app, :ref:`connect to a Location <connect-to-a-location>`
   choosing Twitter as the Channel.
#. When the *Provide Application Credentials* screen comes up, go back to
   https://dev.twitter.com/apps, select your app and visit the *Keys and
   Access Tokens* tab to copy and paste the *Consumer Key* and the *Consumer
   Secret* and insert it in the *Provide Application Credentials* form.

Issues
------

Please post reports, questions, suggestions, etc. at
https://github.com/CampaignChain/campaignchain/issues.

.. _Twitter: https://twitter.com/
.. _campaignchain/channel-twitter: https://github.com/CampaignChain/channel-twitter
.. _campaignchain/location-twitter: https://github.com/CampaignChain/location-twitter
.. _campaignchain/activity-twitter: https://github.com/CampaignChain/activity-twitter
.. _campaignchain/operation-twitter: https://github.com/CampaignChain/operation-twitter
.. _Symfony bundles: http://symfony.com/doc/current/bundles.html