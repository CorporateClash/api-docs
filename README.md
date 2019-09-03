[![StackShare](https://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/corporate-clash/corporate-clash-website)

# TTCC Api Docs
Documentation for the Corporate Clash APIs

### Rate limit

 Our site-wide policy is 20 requests every 1-5 minutes, however this may change based on the URL you're hitting. We recommend you rate limit yourself, as hitting the rate limit will reset your countdown and might prevent access for another few minutes. We have other internal rate limits that aren't listed here that only block the most grevious of bots, should you run into these let us know at our support email.


### Common issues

- Cloudflare Non-JSON/5xx/Interstellar page

Cloudflare plays a big part in our operations, including protecting our web servers from various DDOS attacks and other types of threats. Due to this, your automated district API might (inadvertantly) be blocked by Cloudflare. 

By default, our security level is set to "high" for most of our API, while some more "static" routes are set to medium. See [this article](https://support.cloudflare.com/hc/en-us/articles/200170056-What-does-Cloudflare-s-Security-Level-mean-) for more information, but the general idea is that if your IP address has performed any malicious behavior or automated scanning of the web, your IP address will likely be given a high IP reputation score. This will generally prevent you from accessing almost any Cloudflare protected website, including our own.

To prevent this from happening, be sure to:

- Don't use shared hosting - hosts that share IP addresses among multiple customers usually have at least one user abusing this to send spam and hurt that IP address's reputation, which will affect your own IP score.
- Use a reputable host that doesn't turnover IP addresses so quickly. Providers like AWS, Digitalocean, Google and other reputable hosts generally will wait at least a month before allowing an inactive IP address of another customer to be re-assigned to a new customer. These established hosts also are usually in contact with Cloudflare and other IP reputation companies to ensure they don't give a customer a previously malicious IP address until the reputation has been cleared.

### Special cases

If you have a specific use case and would like to partner with us to remove the rate limit and be whitelisted in Cloudflare, send an email to `support`@corporateclash.net including information about your application, you, and why you need the rate limit removed. 


### Reporting Issues

To report issues not related to security, or to report issues with the API docs, feel free to make an issue.

To report a security issue, email [security@corporateclash.net](mailto:security@corporateclash.net).

