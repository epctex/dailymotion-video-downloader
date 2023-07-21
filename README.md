[https://apify.com/epctex/dailymotion-video-downloader](https://apify.com/epctex/dailymotion-video-downloader?fpr=yhdrb)

# Actor - Dailymotion Video Downloader

## Dailymotion Video Downloader

Since Dailymotion doesn't provide a good and free API, this actor should help you to download videos from Dailymotion.com

The Dailymotion Video Downloader supports the following features:

-   Download Video - If you want to get videos on a certain URL, just type the URL.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/dailymotion-video-downloader/issues).


## Input Parameters

The input of this scraper should be JSON containing the list of pages on Dailymotion.com that should be visited. Required fields are:

- `startUrls`: (Optional) (Array) List of Dailymotion URLs. You should only provide post URLs.

- `quality`: (Optional) (String) Select the video quality. You can use `highest`, `medium`, and `lowest`.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

- `extendOutputFunction`: (Optional) (String) Function that takes a JQuery handle ($) as an argument and returns an object with data.

- `customMapFunction`: (Optional) (String) Function that takes each object's handle as an argument and returns the object with executing the function.

This solution requires using **Residential Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Tips

- You must use a residential proxy to fetch videos. 

- When you want to scrape over a specific list URL, just copy and paste the link as one of the **startUrl**.

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape as many items as possible. Therefore, it forefronts all the detailed requests. If the actor doesn't block very often it'll scrape 1 video under 45 seconds with ~0.01-0.02 compute units.

### Dailymotion Video Downloader Input example

```json
{
  "startUrls": [
    "https://www.dailymotion.com/video/x8j23e4"
  ],
  "quality": "medium",
  "proxy": {
    "useApifyProxy": true
  }
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Dailymotion Video Downloader Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from Dailymotion Video Downloader.

The structure of each item in Dailymotion looks like this:

### Item Detail

```json
{
	"sourceUrl": "https://www.dailymotion.com/video/x8j23e4",
	"downloadUrl": "https://api.apify.com/v2/key-value-stores/46969e17-1fb4-4575-a355-848079fed03b/records/0425d55ffd75c1f151ff9402e8515a9a.mp4"
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.
