Quirk Volkswagen MA Trade Appraisal 
--------------------------------------------------------------
- Primary site link updated to: https://www.quirkvw.com
- Suggested Netlify site name: quirkvwtrade (or quirk-vw-ma-trade)
- All visible "Quirk Subaru" strings replaced with "Quirk Volkswagen MA"
- Success page CTA updated to return to Quirk Volkswagen MA

Deployment checklist:
1) Create a new GitHub repo (e.g., quirk-trade-appraisal-vw-ma) and push this folder.
2) In Netlify, create a new site from that repo. Suggested site name: quirkvwtrade.
3) In index.html & success/index.html, verify links and logo if you want a VW-specific asset (current assets use generic Quirk branding).
4) Set environment variables in Netlify > Site settings > Build & deploy > Environment:
   - SENDGRID_API_KEY = <your key>
   - FROM_EMAIL       = sales@quirkcars.com (or another verified sender)
   - TO_EMAIL         = comma-separated list of recipients (e.g. mpalmer@quirkcars.com, gmcintosh@quirkcars.com, lmendez@quirkcars.com)
   - (Optional) SHEETS_WEBHOOK_URL and SHEETS_SHARED_SECRET for Google Sheets backup
5) Test English/Spanish toggles; success page should match the selected language.
6) Test VIN decode, file uploads, and email delivery (the function posts to /api/trade-appraisal).
