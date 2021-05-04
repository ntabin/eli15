# Cache-Aside Pattern

When your app or program gets its data from a database or from a backend service, you need to use cache layer to help your app run quickly. Cached data are usually data that are not changed frequently.

If your app needs a data from a database or from a backend service, it first:
* Check data in the cache if available. If yes then good it will just use that data.
* If not then fetch it from a database or from a backend service then write it in the cache.

The concern here is when should a cache data expire or when should it fetch again the data so it will be up to date. The solution here is to setup a **_TTL (Time to live)_**. 
You must just set it in the right interval. If you set it too low, your app might be bombarding request to your database or backend service and just getting the same cache data. 
Or if too long your app data will remain not updated for a long time. There is no silver bullet on this onen so one should plan carefully.

If your app only uses static data then there is no need to use this pattern. My way of increasing app performance are:
* Just set the cached data to not expire
* load everything you need in startup
