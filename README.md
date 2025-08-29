# DynDNS Update Forwarding Server

Small http server that receives dyndns update requests and forwards them to multiple DynDNS providers.

Written in Python using `aiohttp` and `fastapi`; running on `uvicorn`.

Tailored towards receiving requests from a FritzBox.
