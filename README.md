# Atoresume (آتورزومه)

Atoresume is a lightweight, high-performance, single-page client-side resume builder web application. It features automated real-time previewing, layout orchestration, multi-language rendering, and dynamic page-budget calculations designed to align natively with standardized A4 dimensions.

## Key Technical Features

* **Real-Time Live Compilation:** Instant synchronization between structural DOM inputs and client-side view representation via precise layout update lifecycles.
* **Dynamic Page Budgeting & Section Splitting:** Algorithmic calculation of heights for structured content blocks, seamlessly grouping or wrapping multi-page resumes across separate native A4 frames to prevent overflow.
* **ATS Compatibility Metric Engine:** Implements a localized programmatic weighting scanner to audit resume data fields against standard Application Tracking System requirements.
* **Pure Native Multi-Format Exporters:**
    * **PDF Exporter:** Injects structural CSS printing stylesheets dynamically to trigger explicit A4 frame fragmentation via `window.print()`.
    * **Word (DOC) Generation:** Micro-compiles complete structured HTML schemas using standard binary representations (`\ufeff` BOM payload) embedded directly inside data blobs for native Microsoft Word ingestion.
* **State Portability via Serialization:** Features native JSON orchestration enabling complete data structure export, payload safe-clipping, and state recovery.
* **Responsive Multi-Device Adaptability:** Real-time container matrix scaling matching arbitrary view ports while reserving high-definition 794px by 1123px proportions on production print profiles.

## Architecture & System Requirements

The application runs entirely on standard web clients, adhering to zero-dependency development principles.

* **Client Core:** HTML5, CSS3 Custom Variables (Design Tokens)
* **Engine Core:** JavaScript (ECMAScript 6+)
* **Typography Subsystem:** Google Fonts (Vazirmatn / Markazi Text CDN integrations)

## Implementation & Quick Start

Since the infrastructure requires no compilation, the application can be served instantly via any static file server or embedded locally.

```bash
git clone [https://github.com/miladbasery/Atoresume.git](https://github.com/miladbasery/Atoresume.git)
cd Atoresume
python3 -m http.server 8000
```

## JSON Schema Specification

```
JSON
{
  "photo": "data:image/svg+xml;base64,...",
  "fname": "String",
  "lname": "String",
  "jobtitle": "String",
  "speciality": "String",
  "birthdate": "String",
  "marital": "String",
  "city": "String",
  "country": "String",
  "address": "String",
  "phone": "String",
  "email": "String",
  "website": "String",
  "linkedin": "String",
  "github": "String",
  "instagram": "String",
  "telegram": "String",
  "twitter": "String",
  "youtube": "String",
  "about": "String",
  "objective": "String",
  "work": [
    {
      "company": "String",
      "position": "String",
      "period": "String",
      "duties": "String",
      "url": "String",
      "type": "String",
      "logo": "String"
    }
  ],
  "education": [],
  "projects": [],
  "courses": [],
  "hardSkills": [
    { "name": "String", "pct": 85 }
  ],
  "softSkills": [],
  "languages": [],
  "sectionOrder": ["about", "work", "education", "projects", "courses"],
  "sectionHidden": {},
  "themeIdx": 0
}
```
## License
This software utility is distributed under open-source compliance terms. Review the repository metadata for comprehensive licensing specifications.
