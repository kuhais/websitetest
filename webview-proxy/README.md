# WebView Proxy

A responsive GitHub Pages frontend for loading sites through your Cloudflare Worker proxy.

## GitHub Pages

1. Create a repository and upload this project to the repository root.
2. Open **Settings → Pages**.
3. Select **GitHub Actions** as the source.
4. Push the included workflow below, or enable Pages and deploy the root directory with a Pages workflow.

## Proxy

The app uses your Worker:
`https://fragrant-rain-3092.kuhaisthebest.workers.dev/?proxyUrl=`

The destination URL is URL-encoded before being appended.

## Notes

Some sites cannot be embedded or proxied cleanly because of CSP, authentication, JavaScript behavior, WebSockets, or other browser/security controls. Your Worker also needs to return the proxied content with headers that permit this use.
