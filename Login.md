## Login API


The login api is used to log players into the game via the official launcher or a third-party launcher. Note that while this API may work with unofficial launchers, we cannot guarantee that it will be not be changed without warning.

This is version 1 of the API and does not support the Launcher token authentication system. This might be documented in the future, but for now this API should continue to work.

#### Request

Endpoint: 

    POST https://corporateclash.net/api/v1/login/:username

|Params|Description|
|--|--|
|`password`|The user's password.|

#### Response

```json
{
  "status": true,
  "reason": 0,
  "friendlyreason": "Welcome back to Toontown, :username!",
  "token": "20514397d70d8fb99e021a5f28fbeba3fc29814ec452ef1a3a3fcf42b08bb752"
}
```

|Field|Type|Description|
|--|--|--|
|`status`|boolean|True if the login was successful|
|`reason`|integer|Unique number associated with the error when `status` is false|
|`friendlyreason`|string|A user-friendly error/success message. If `status` is true, you may show a custom success message.|
|`token`|string|The login token that should be used by the game|

#### Post-Success Login

When a user successfully authenticates and `status` is true, the game needs to start up. This is done via environment variables set in a process-specific context.

Required env vars:

* `TT_GAMESERVER`: set to `gs.corporateclash.net`
* `TT_PLAYCOOKIE`: set to the `token` variable from above

These must be set in the game/launcher process before starting it.
