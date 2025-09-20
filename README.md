# silverlanternslight

A Cloudflare Worker site template for serving static content.

## Development

To start the development server:

```bash
npm run start
```

This runs `wrangler dev` to start a local development server.

## Deployment

To deploy the worker to Cloudflare:

```bash
npx wrangler deploy
```

This command will:
- Build and deploy your worker to Cloudflare's edge network
- Deploy static assets from the `./public` directory
- Make your site available at the configured route: `www.silverlanternslight.com/*`

### Prerequisites for Deployment

1. **Cloudflare Account**: You need a Cloudflare account with the appropriate permissions
2. **Authentication**: You must be logged in to Wrangler:
   ```bash
   npx wrangler login
   ```
3. **Zone Configuration**: Ensure your domain `silverlanternslight.com` is properly configured in your Cloudflare dashboard

## Configuration

The deployment is configured via `wrangler.toml`:
- **Worker Name**: `worker-sites-template`
- **Main Script**: `src/index.js`
- **Static Assets**: Files in `./public` directory
- **Route**: `www.silverlanternslight.com/*`
