## Districts

Districts can get the current population of the game (via adding the population of all district objects sent) as well as any current invasions.

Endpoint

    https://corporateclash.net/api/v1/districts


Note that data returned may be delayed by up to 20 seconds due to cloudflare's short-lived 15 second cache plus any delays with districts polling their status.


#### Response


```json
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
