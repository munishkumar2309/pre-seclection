Bajaj Capital Prescreener - CloudFront Upload Instructions

Deploy target:
https://prescreener.bajajcapitalinsurance.com/

Upload the CONTENTS of this folder to the S3/CloudFront origin root.
Do not upload the parent folder itself.

Required files in origin root:
- index.html
- disc.html
- refer.html
- favicon.ico
- favicon-32x32.png
- apple-touch-icon.png
- bajaj-logo-2025.png

Important CloudFront settings:
1. Default root object: index.html
2. Query strings must be forwarded/preserved for disc.html.
   Required parameters include candidate_id, token, lang, preferred_language.
3. After upload, invalidate CloudFront cache with: /*
4. Favicon links use cache-busting version: 20260622v6

Functional fixes included:
- Hindi selected in preselection is forced into DISC links as lang=hi and preferred_language=hi.
- English remains default when no language is selected.
- Favicon is linked with relative paths so it works on CloudFront and local testing.
