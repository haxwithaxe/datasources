Live traffic camera footage from https://chart.maryland.gov/TrafficCameras/GetTrafficCameras.

Their API has lots of other info on MDOT stuff like road closures and traffic incidents.


# Docs
https://chart.maryland.gov/DataFeeds/GetDataFeeds

To get the video feed without the webUI:
1. Go to https://chart.maryland.gov/TrafficCameras/GetTrafficCameras look up the camera you want the feed from.
1. Go to https://chartexp1.sha.maryland.gov/CHARTExportClientService/getCameraMapDataJSON.do and `Ctrl+f` to find the entry for the camera using the description.
1. Copy the URL from the `publicVideoUrl` field and use it in an iframe or browser window.


# Examples
## Get the URL for the camera at I-495 and Connecticut Ave exit 33
1. Following step 1 above we find the description contains ``Ex 33``.
1. Step 2 searching the JSON for ``Ex 33`` gets us the following entry.

        ```json
        {
            "data": [
                ...
                {
                    "cameraCategories": [
                        "Wash. DC"
                    ],
                    "cctvIp": "strmr5.sha.maryland.gov",
                    "commMode": "ONLINE",
                    "description": "I-495 W. of Ex 33 MD 185 Connecticut Ave",
                    "id": "e301515800f700d700437a45351f0214",
                    "lastCachedDataUpdateTime": 1754329716761,
                    "lat": 39.007416,
                    "lon": -77.08681,
                    "milePost": 7.7,
                    "name": "315003",
                    "opStatus": "OK",
                    "publicVideoURL": "https://chart.maryland.gov/Video/GetVideo/e301515800f700d700437a45351f0214",
                    "routeNumber": 495,
                    "routePrefix": "IS",
                    "routeSuffix": ""
                },
                ...
            ]
        }
        ```

1. Step 3 gets us the URL ``https://chart.maryland.gov/Video/GetVideo/e301515800f700d700437a45351f0214``.


Keywords: traffic camera, surveilance, video
