# DynDNS Update Forwarding Server

Small http server that receives dyndns update requests and forwards them to multiple DynDNS providers.

Written in Python using `aiohttp` and `fastapi`; running on `uvicorn`.

Tailored towards receiving requests from a FritzBox.

## DynDNS failures in FritzBox log

The FritzBox might be sending requests right after a reconnect, upon which requests initiated by this server might hang for a while.
This might cause the FritzBox to timeout the request, log a dyndns update failure and send another one.
This *should* be fine, unless the providers start rate limiting us ...
