DFWIN V2 HOTFIX — Nov 5, 2026

1. GitHub root: replace index_V2.html only. This masks leftover lettering baked into the cruise-ship background. Keep hero_ship.jpg unchanged.

2. Google Apps Script RFQ RECEIVER project (not GitHub): open RFQ_Form.html, replace its entire content with the supplied RFQ_Form.html, Save. Deploy > Manage deployments > Edit (pencil) > Version: New version > Deploy. Make sure the original public web app /exec URL stays the same. Do not paste this file into GitHub. Do not edit the private catalog publisher.

3. Test: add two catalog products with quantities, open basket, Continue to Contact & Quote Form. Both items + quantities should show in section 2, and Review request should be enabled. Complete required details, click Review request, then Submit inquiry to DFWIN.

Reason for issue: The Apps Script injected prefill can be a JSON string rather than an object; the old RFQ_Form.html accessed prefill.items without parsing the string and silently discarded items. The updated form parses both formats and carries quantity into the form.
