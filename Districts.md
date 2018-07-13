## Districts

Districts can get the current population of the game (via adding the population of all district objects sent) as well as any current invasions.

Endpoint

    https://corporateclash.net/api/v1/districts


Note that data returned may be delayed by up to 20 seconds due to cloudflare's short-lived 15 second cache plus any delays with districts polling their status.


#### Response


```json
[
    {
        "name": "Kooky Ville",
        "population": 7,
        "invasion_online": false,
        "last_update": 1531460716,
        "cogs_attacking": "None",
        "count_defeated": 0,
        "count_total": 0,
        "remaining_time": 0
    },
    {
        "name": "Wacky Ville",
        "population": 0,
        "invasion_online": true,
        "last_update": 1531462136,
        "cogs_attacking": "Telemarketer",
        "count_defeated": 6,
        "count_total": 1000,
        "remaining_time": 754
    }
]
```
