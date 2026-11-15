# Deployment — verification required

No deployment settings were changed as part of the documentation branch.

## Before documenting as fact
- Confirm Netlify site ID/name and linked GitHub repository.
- Confirm production branch, build command (if any), publish directory, deploy previews and redirects.
- Confirm custom domains, authoritative DNS provider, TLS and relevant headers.
- Record environment variable **names only**; never paste values or tokens.
- Verify rollback procedure using Netlify deployment history.

## Release checklist
- Review PR diff and run validation checks.
- Inspect Netlify deploy preview on desktop/mobile; test links, accessibility and metadata.
- Obtain explicit approval before merging into production branch.
- Confirm deployment result and document rollback reference.
