# Deployment Checklist

## React Static Site

- Set the build command and publish directory that match the selected React setup.
- Define the deployed API URL as a client environment variable.
- Configure SPA route rewriting so refreshing a client route does not return 404.

## Express Web Service

- Ensure the server listens on `process.env.PORT`.
- Add MongoDB URI, session secret, client URL, and other required variables in the hosting dashboard.
- Allow the exact deployed client origin through CORS.
- When cross-site cookies are required, configure client credentials, server CORS credentials, and production cookie options consistently.

## Verification

Test in a private/incognito window:

1. Open the React URL.
2. Register and log in.
3. Create a record.
4. Refresh the page and verify the session/data remain available as intended.
5. Update and delete an owned record.
6. Verify another account cannot update or delete it.
7. Open the API base URL or a public GET endpoint and confirm an expected response.
