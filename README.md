See [taiga](https://github.com/docker-taiga/taiga) for usage information.

This fork sets nginx to work only in http, useful if you want an external proxy to manage https. Here is an Apache2 example (only relevant lines are shown, change [PORT] as needed):

```
ProxyPreserveHost On
ProxyPass /events ws://localhost:51553/events
ProxyPass / http://localhost:[PORT]/
ProxyPassReverse / http://localhost:[PORT]/
```
