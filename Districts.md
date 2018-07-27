## Districts

Districts can get the current population of the game (via adding the population of all district objects sent) as well as any current invasions.

Endpoint

    https://corporateclash.net/api/v1/districts


Note that data returned may be delayed by up to 30 seconds due to cloudflare's short-lived 15 second cache plus any delays with districts polling their status.


#### Response

returns a JSON array of district objects

**district object**

|Field|Type|Description|
|--|--|--|
|`name`|string|District Name|
|`online`|boolean|Generally always true. Districts are removed if they don't report their status after a few minutes.|
|`population`|int|District population|
|`invaison_online`|boolean|True if invasion is in district|
|`last_update`|int|Unix time for last updated. Propably UTC.|
|`cogs_attacking`|string|Cog attacting name. A list of cog names will be added here in the future.|
|`count_defeated`|int|Amount of cogs defeated in the district|
|`count_total`|int|Total amount of cogs allocated to the invasion.|
|`remaining_time`|int|Amount of time before invasion automatically reboots, in seconds|

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
