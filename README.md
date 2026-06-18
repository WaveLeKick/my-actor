[My Actor](https://apify.com/established_zabra/my-actor?fpr=data)

## Overview

The **Fake Candidate Checker** is an Apify actor designed to analyze LinkedIn profiles for **potential hiring fraud risk indicators** using **metadata-based heuristics**, explainable scoring, and optional limited public access checks.

The actor is built to remain reliable even when LinkedIn restricts automated access by falling back to **non-invasive metadata-only analysis** instead of failing or attempting aggressive scraping.

This makes it suitable for **HR teams, recruiters, staffing agencies, and hiring managers** who want early signals about profiles that may require additional verification.

---

## What Problem Does This Solve?

Modern hiring processes increasingly face challenges such as:

- Fake or misrepresented candidates
- Auto-generated or incomplete LinkedIn profiles
- Inconsistent public profile signals
- Increased risk in remote hiring workflows
- Wasted interview and onboarding effort

This actor helps teams **identify profiles that may require enhanced screening** before progressing further in the hiring pipeline.

---

## Key Features

- ✅ Metadata-only analysis (no LinkedIn login required)
- ✅ Graceful handling of LinkedIn access restrictions
- ✅ Explainable risk scores with clear flags
- ✅ Store-safe, non-invasive design
- ✅ Works reliably even when LinkedIn blocks access
- ✅ Suitable for compliance-sensitive environments

---

## How It Works

1. Accepts one or more LinkedIn profile URLs
2. Optionally attempts limited public data access
3. If LinkedIn restricts access, switches to metadata-only heuristics
4. Assigns a probabilistic **risk score**
5. Outputs detected risk indicators and recommended next steps

---

## Input

### Example Input

```
{
  "linkedinUrls": [
    "https://www.linkedin.com/in/example-profile/"
  ],
  "metadataOnly": true
}

### Example Outputs
{
  "linkedinUrl": "https://www.linkedin.com/in/example-profile/",
  "mode": "metadata-only",
  "riskScore": 45,
  "flags": [
    "Limited public LinkedIn visibility",
    "Suspicious numeric-heavy profile handle"
  ],
  "recommendation": "Manual review recommended",
  "disclaimer": "This tool provides probabilistic risk indicators only and does not confirm fraud."
}
```