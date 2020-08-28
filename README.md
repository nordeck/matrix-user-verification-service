# Matrix User Verification Service

Service to verify details of a user based on a Open ID Connect token.

Main features:

* Verifies a C2S [Open ID token](https://matrix.org/docs/spec/client_server/r0.6.1#id154)
  using the S2S [UserInfo endpoint](https://matrix.org/docs/spec/server_server/r0.1.4#openid).
* Can verify user is a member in a given room (Synapse only currently, requires admin level token).

## How to use

### Dependencies

```
npm install
```

### Configuration

Copy the default `.env.default` to `.env` and modify as needed.

```
# Admin token (synapse only)
# Required for the service to verify room membership
UVS_ACCESS_TOKEN=foobar
# Homeserver URL
UVS_HOMESERVER_URL=https://matrix.org
# (Optional) listen address of the bot
UVS_LISTEN_ADDRESS=127.0.0.1
# (Optional) listen port of the bot
UVS_PORT=3000
```

### Running

```
npm start
```

### Development

Run in watch mode.

```
npm dev
```

## License

Apache 2.0
