# Common Issues

## Client Cannot Reach API

- Check the deployed API URL and protocol.
- Confirm the client environment variable was available during the build.
- Inspect the browser Network tab for the actual request URL and response.

## CORS Error

- Allow the exact client origin, including `https://` and without an incorrect trailing path.
- Enable credentials on both client requests and server CORS configuration when using cookies.
- Do not combine a wildcard origin with credentialed requests.

## Login Works Locally but Not After Deployment

- Confirm the session secret is configured on the server.
- Check cookie `secure` and `sameSite` options for the deployed arrangement.
- Confirm the browser request includes credentials.
- Check whether the hosting service restarted or lost an in-memory session. Use an appropriate persistent session store if required by the implementation.

## MongoDB Connection Fails

- Check the connection string in the hosting environment.
- Confirm the database user, password, and network-access settings.
- URL-encode special characters in credentials.
- Do not paste the real connection string into GitHub, screenshots, reports, or AI prompts.

## Deployed Service Appears Slow Initially

Some free hosting services may pause inactive services. Wait for the first request to complete, then test again. Do not repeatedly change working code before checking service logs.

## Route Refresh Returns 404

Configure the static host to rewrite unknown client routes to `index.html` so React Router can handle them.

## Debugging Method

1. Reproduce one problem at a time.
2. Read the first meaningful error in the browser console, Network tab, or server logs.
3. Identify whether the failure is in the client, network/configuration, server, or database.
4. Make one focused change and retest.
5. Record significant AI assistance in `AI-USE.md`.
