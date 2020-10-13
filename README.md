# Tarta Business Intelligence (BI)


## Overview

### Who can help me?
If you have questions, you can always [email](mailto:support@tarta.ai) or skype us(taras_00)! If you found a bug feel free to [create an issue](https://github.com/tarta-ai/bi/issues). 

## Getting Started
This is a simplified walkthrough to see the platform in action.  To see the complete API Documentation please see our Swagger page https://app.swaggerhub.com/apis-docs/T15413/Tarta-BI/1.0.1-oas3.

## API

The Tarta API uses API keys to authenticate requests. You can view and manage your API keys in the Stripe Dashboard.

Test mode secret keys have the prefix sk_test_ and live mode secret keys have the prefix sk_live_. Alternatively, you can use restricted API keys for granular permissions.

Your API keys carry many privileges, so be sure to keep them secure! Do not share your secret API keys in publicly accessible areas such as GitHub, client-side code, and so forth.

Authentication to the API is performed via HTTP Basic Auth. Provide your API key as the basic auth username value. You do not need to provide a password.

If you need to authenticate via bearer auth (e.g., for a cross-origin request), use -H "Authorization: Bearer sk_test_J6r3iPnezDwdXv4YuvOT97GO00lRmLgblP" instead of -u sk_test_J6r3iPnezDwdXv4YuvOT97GO00lRmLgblP.

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

### Schema
All API access is over HTTPS, and accessed from the `https://api.tarta.ai/bi/`. All data is sent and received as JSON.

##### Full INCOMING, ECHO and READ request example(copy, paste and execute it)
```
POST https://api.tarta.ai.co/bi/v1/views/ HTTP/1.1
Content-Type: application/json
Authorization: [your Basic auth token here]

{
  "job": {
    "created": "2020-09-16T21:03:19.7304756Z",
    "isRemote": true,
    "id": "qvi6mHQBkC4zA6UN2duJ",
    "name": "Senior Software Developer - iOS (Remote)",
    "urlName": "senior-software-developer-ios-remote-2",
    "titleTags": [
      "senior",
      "software",
      "developer",
      "ios"
    ],
    "tags": [
      "mobile",
      "data",
      "startup",
      "machine learning",
      "cad",
      "row",
      "google"
    ],
    "profile": "senior software developer",
    "isActive": true,
    "employmentType": [
      "FULL_TIME"
    ],
    "location": null
  },
  "company": {
    "id": "5de7cd5f525d5d07d8318ac4",
    "name": "Hopper",
    "urlName": "hopper"
  },
  "source": 2002,
  "utm_source": null,
  "utm_medium": null,
  "utm_campaign": null,
  "referral": "dev.tarta.ai",
  "userAgent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/85.0.4183.121 Safari/537.36 Edg/85.0.564.70",
  "isRobot": false,
  "type": "job",
  "ip": "127.0.0.1",
  "url": "/company/hopper/job/senior-software-developer-ios-remote-2",
  "published": {
    "google": "2020-09-16T21:03:20.0886012Z",
    "bing": null
  }
}
```
