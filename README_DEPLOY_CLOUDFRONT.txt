DEPLOYMENT INSTRUCTIONS

This package is ROOT READY. Upload these files directly to the S3/CloudFront origin root.

After upload, these URLs must work:
- https://prescreener.bajajcapitalinsurance.com/
- https://prescreener.bajajcapitalinsurance.com/index.html
- https://prescreener.bajajcapitalinsurance.com/disc.html
- https://prescreener.bajajcapitalinsurance.com/refer.html
- https://prescreener.bajajcapitalinsurance.com/favicon.ico
- https://prescreener.bajajcapitalinsurance.com/favicon-32x32.png

Do not upload a parent folder. The files in this zip must sit at bucket root.

CloudFront settings:
- Default root object: index.html
- Preserve/forward query strings for disc.html
- Invalidate cache after deploy: /*

Reason for this version:
- Fixes Cannot GET /disc.html by packaging disc.html at root.
- Fixes favicon by putting favicon.ico and favicon PNGs at root and using absolute /favicon paths.
- Requires matching n8n workflow JSON to force DISC links to https://prescreener.bajajcapitalinsurance.com/disc.html.
