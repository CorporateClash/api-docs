## Districts

Districts can get the current population of the game (via adding the population of all district objects sent) as well as any current invasions.

Endpoint

    https://corporateclash.net/api/v1/districts.js

The `.js` extension is only so that we may use the Cloudflare cache, and the data returned is not javascript ([why?](https://support.cloudflare.com/hc/en-us/articles/200172516-Which-file-extensions-does-Cloudflare-cache-for-static-content-#h_a01982d4-d5b6-4744-bb9b-a71da62c160a)).

Note that data returned may be delayed by up to 20 seconds due to the Cloudflare cache and the delay of districts polling their status.


#### Response

returns a JSON array of district objects

**district object**

|Field|Type|Description|
|--|--|--|
|`name`|string|District Name|
|`online`|boolean|Generally always true. Districts are removed if they don't report their status after a few minutes.|
|`population`|int|District population.|
|`invasion_online`|boolean|True if invasion is present in district.|
|`last_update`|int|Unix time for last updated. Probably UTC.|
|`cogs_attacking`|string|Cog attacking name. A list of cog names will be added here in the future.|
|`count_defeated`|int|Amount of cogs defeated in the district.|
|`count_total`|int|Total amount of cogs allocated to the invasion.|
|`remaining_time`|int|Amount of time before invasion automatically ends, in seconds.|

If you encounter issues with the data, create an issue on this github repo.

```json
[
    {
	    "name": "Feather Field",
		"online": true,
		"population": 38,
		"invasion_online": false,
		"last_update": 1531491404,
		"cogs_attacking": "None",
		"count_defeated": 328,
		"count_total": 0,
		"remaining_time": 0
	},
	{
		"name": "Bamboozle Bay",
		"online": true,
		"population": 48,
		"invasion_online": true,
		"last_update": 1531491403,
		"cogs_attacking": "Pencil Pusher",
		"count_defeated": 5,
		"count_total": 3522,
		"remaining_time": 1774
	}
]
```
