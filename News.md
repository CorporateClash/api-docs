## News

Gets the most recent articles published on our website.

#### Articles

Endpoint

    GET https://corporateclash.net/api/v1/launcher/news
    
    
#### Single Article


Endpint


    GET https://corporateclash.net/api/v1/launcher/news/:newsid
    

#### Response

Always returns an array of article objects, even if requesting a single news article.


```json
[
	{
		"id": 4,
		"author": "Corporate Clash Team",
		"posted": "2018-03-09 22:30:33",
		"title": "There's a New Chef in Town!",
		"summary": "Hi there toons! Loopy Goopy Googlenerd here. And I'm not here just for vanity, I got a real reason! My shop's offici...",
		"category": "Blog"
	},
	{
		"id": 3,
		"author": "Corporate Clash Team",
		"posted": "2018-02-28 20:18:50",
		"title": "Painters Programmers, and Texture Artists.",
		"summary": "Toontown Corporate Clash is the next new server on the horizon, but we're in need of talented, interested artists and...",
		"category": "Blog"
	}
]
```
