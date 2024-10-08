---
layout: example
title: Do not forget link focus states
description: Links must be distinct when focused and with sufficient colour contrast. This can get missed if manually rebuilding GOV.UK Frontend manually (for example if using a Javascript framework) or using an old version of GOV.UK Frontend.
tags: "Code"
wcag:
- text: "WCAG 2.2 2.4.7: Focus Visible (Level AA)"
  link: https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html
mistake:
- link: link-focus/mistake
  description: This example is most likely to happen if the GOV.UK Frontend is being rebuilt in a codebase as an abstraction rather than using default templates.
  reason: Not having 'govuk-link' style or similar may mean a link does not have have sufficient contrast in the focus state.
- link: link-focus/mistake-2
  description: If a service has not been updated for a while, its frontend may be out of date.
  reason: Earlier versions of GOV.UK Frontend used a focus style that did not meet colour contrast standards. It has since been updated.

improvement:
- link: link-focus/improved
  reason: The link now has a clear and accessible focus when tabbed. This fix is done by adding 'class="govuk-link"' to the link and making sure that the service is using a recent version of GOV.UK Frontend.
links:
    - text: Use sufficient colour contrast - older versions of GOV.UK Frontend (DWP Accessibility manual)
      href: https://accessibility-manual.dwp.gov.uk/guidance-for-your-job-role/interaction-designer#use-sufficient-colour-contrast

---
