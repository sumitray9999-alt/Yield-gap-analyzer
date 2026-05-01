[README.md](https://github.com/user-attachments/files/27275163/README.md)
# 🌽 Maize Yield Gap Analyser

> **AI-powered yield gap diagnosis for Indian farmers — free, fast, and field-ready.**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Crops Covered](https://img.shields.io/badge/Crops-8-yellow)](README.md)
[![States Covered](https://img.shields.io/badge/States-29-blue)](README.md)
[![Powered by Claude](https://img.shields.io/badge/AI-Anthropic%20Claude-green)](https://anthropic.com)

The **Maize Yield Gap Analyser** is a single-file web application that diagnoses the gap between a farmer's actual crop yield and the scientifically established state-level yield potential — then assigns a rupee value to each limiting factor and delivers an AI-generated, evidence-based corrective action plan. Built on agronomic benchmarks for all 29 Indian states and powered by Anthropic Claude, the tool turns complex crop science into simple, farm-ready decisions in under 2 minutes.

---

## 📲 Download & Install (Android APK)

> ⚠️ This app is distributed outside the Google Play Store.  
> You must enable **"Install from Unknown Sources"** before installing.

### Installation Steps
1. [**⬇️ Download the latest APK**](https://github.com/SumitRay/maize-yield-gap-analyser/releases/latest)
2. On your Android phone:  
   `Settings → Security → Enable "Install from Unknown Sources"`
3. Open the downloaded `.apk` file → Tap **Install**
4. Open the app — no sign-up, no login required

> ✅ Requires **Android 6.0 (Marshmallow) or higher**

---

## 🌾 What is a Yield Gap?

The yield gap is the difference between what a crop *could* produce and what it *actually* produces on a given farm. This app measures three reference points:

| Term | Definition |
|------|-----------|
| 🏆 **State Yield Potential (Yp)** | Maximum achievable yield for the crop under best management in the state — adjusted for local agro-ecology |
| 📊 **District Average (Ya̅)** | Mean yield for comparable farms in the region |
| 🌾 **Your Actual Yield (Ya)** | What you harvested this season |

**Yield Gap = Yp − Ya**

Closing this gap is the most cost-effective, land-neutral pathway to improving farm income and national food security.

---

## ✨ Key Features

### 🔬 Scientific Yield Gap Computation
The app computes individual yield-limiting factors using crop- and state-specific agronomic benchmarks:

| Factor | Basis |
|--------|-------|
| Variety / Seed Quality | Penalty matrix for OPV, farm-saved, state-released vs certified hybrid |
| Late Sowing / Planting | Sowing delay loss function (1–2 wk, 3–4 wk, >4 wk) |
| Nitrogen (N) Deficiency | N response coefficients per crop; benchmark N dose per state |
| Phosphorus (P₂O₅) Deficiency | P response coefficients; benchmark P dose per crop |
| Water Stress | Irrigation deficit model across critical crop growth stages |
| Weed Competition | Weed management quality matrix (herbicide → no management) |
| Pest & Disease Damage | Incidence severity scale (none → severe >50%) |

### 📈 Yield Performance Score
An aggregated **yield score (0–100)** benchmarks the farmer against state potential, with intuitive grade labels:

| Score | Grade |
|-------|-------|
| 0–30 | 🔴 Critical — Urgent attention needed |
| 31–50 | 🟠 Below average — Large yield gap |
| 51–70 | 🟡 Fair — Moderate improvement possible |
| 71–85 | 🟢 Good — Above average management |
| 86–100 | 💚 Excellent — Near-optimal performance |

### 💰 Revenue Impact Quantification
Every yield-limiting factor is translated into **lost income in Indian Rupees** at crop-specific market prices (e.g., ₹2,100/q for maize), making agronomic advice immediately actionable in economic terms.

### 🤖 AI Agronomist — Powered by Anthropic Claude
After computing the yield gap, the app consults an AI agronomist (Claude) to generate:
- A **key insight** specific to the farmer's numbers and state
- A **contextual analysis** situating the gap within local agronomy
- A **priority action plan** for next season with timing, dose, and product recommendations
- A **realistic next-season yield target** if the top constraints are addressed

### 🗺️ 29-State Benchmarking
State-specific yield potential and district average multipliers calibrated for all 29 major Indian states — from Punjab and Haryana in the north to Kerala and Tamil Nadu in the south, and from Arunachal Pradesh to Rajasthan.

---

## 🌱 Crops Supported

| Crop | Potential Yield | Key Season | Market Price |
|------|----------------|-----------|-------------|
| 🌽 Maize | 85 q/ha | Kharif / Rabi | ₹2,100/q |
| 🌾 Rice | 70 q/ha | Kharif | ₹2,300/q |
| 🌾 Wheat | 55 q/ha | Rabi | ₹2,400/q |
| 🌿 Cotton | 32 q/ha | Kharif | ₹7,000/q |
| 🫘 Soybean | 30 q/ha | Kharif | ₹4,600/q |
| 🌻 Mustard | 28 q/ha | Rabi | ₹5,650/q |
| 🥜 Groundnut | 35 q/ha | Kharif / Summer | ₹6,500/q |
| 🎋 Sugarcane | 1,100 q/ha | Annual | ₹350/q |

> *Potential yields are base values adjusted by state-specific multipliers for all 29 states.*

---

## 📋 The 11-Question Survey

The app collects the minimum necessary inputs to diagnose a yield gap accurately:

| # | Question | Input Type |
|---|----------|-----------|
| 1 | Which crop are you analysing? | Dropdown (8 crops) |
| 2 | Which state is your farm located in? | Dropdown (29 states) |
| 3 | Which season did you grow the crop? | Radio (Kharif / Rabi / Summer) |
| 4 | What type of seed or planting material was used? | Radio (Certified hybrid → Local/unknown) |
| 5 | How timely was sowing relative to the local optimum? | Radio (On time → >4 weeks late) |
| 6 | Total nitrogen (N) applied this season | Slider (kg N/ha) |
| 7 | Total phosphorus (P₂O₅) applied this season | Slider (kg P₂O₅/ha) |
| 8 | Number of irrigations given to the crop | Slider |
| 9 | How was weed management carried out? | Radio (Herbicide + interculture → None) |
| 10 | How severe was pest and disease incidence? | Radio (None → Severe >50%) |
| 11 | What was your actual yield this season? | Slider (q/ha) |

---

## 🧑‍🌾 Who Is This For?

| User | Use Case |
|------|---------|
| 👨‍🌾 Smallholder Farmers | Understand why yields are low and get a personalised action plan |
| 🔬 Agronomists & Researchers | Rapid field diagnosis and gap quantification |
| 🏛️ KVK & Extension Officers | Science-based recommendations during farm visits |
| 📚 Agronomy Students | Hands-on learning of yield gap concepts with real data |
| 🏢 NGOs & Development Projects | Farmer profiling, monitoring, and evaluation |

---

## 🛠️ Technical Details

| Property | Details |
|----------|---------|
| Technology | Vanilla HTML5 / CSS3 / JavaScript — single file, zero dependencies |
| AI Engine | Anthropic Claude (claude-sonnet) via configurable backend |
| Platform | Android (APK) + any modern web browser |
| Minimum Android | 6.0 (API Level 23) |
| Internet Required | Yes — for AI agronomist analysis |
| Offline Capability | Yield gap computation works offline; AI analysis requires connection |
| Backend Config | Set `window.MAIZE_BACKEND_URL` to point to your API endpoint |
| Fonts | Playfair Display · DM Sans · JetBrains Mono |
| Login / Sign-up | None required |
| Data Storage | Session-only — nothing persisted to any server |

---

## 🚀 Running Locally (Web Browser)

```bash
# Clone the repository
git clone https://github.com/YourUsername/maize-yield-gap-analyser.git

# Open the app directly in your browser
open maize-yield-gap-analyser.html
```

To enable the AI agronomist feature, configure your backend URL:

```html
<!-- Add before closing </body> tag -->
<script>
  window.MAIZE_BACKEND_URL = 'https://your-backend.example.com';
</script>
```

The backend should expose a `POST /api/analyse` endpoint that forwards the prompt to the Anthropic Claude API and returns the parsed JSON result.

---

## 🔬 Scientific & Methodological Basis

This tool is grounded in globally recognised yield gap frameworks:

- **van Ittersum et al. (2013)** — Yield gap analysis with local to global relevance. *Field Crops Research*, 143, 4–17
- **Global Yield Gap Atlas (GYGA)** — [www.yieldgap.org](https://www.yieldgap.org)
- **ICAR Crop Production Guidelines** — State-level N, P, and water benchmarks for India
- **FAO Crop Water Requirements** — Growth-stage irrigation prioritization
- **CIMMYT Maize Agronomy** — Fall armyworm management, hybrid selection, split fertilization

---

## 📦 Releases

| Version | Date | Notes |
|---------|------|-------|
| v1.0.0 | May 2026 | Initial public release |

👉 [View all releases](https://github.com/YourUsername/maize-yield-gap-analyser/releases)

---

## 🔒 Privacy & Permissions

| Permission | Purpose |
|------------|---------|
| 🌐 Internet | Required for AI agronomist analysis |

- ✅ No personal data collected
- ✅ No login or registration required
- ✅ All farm data is session-local — nothing stored on any server
- ✅ Completely free to use

📄 [Privacy Policy](PRIVACY_POLICY.md)

---

## 🤝 Contributing

Bug reports, feature suggestions, and pull requests are welcome.

1. Fork this repository
2. Create a branch: `git checkout -b feature/your-feature-name`
3. Commit changes: `git commit -m "Add: description of change"`
4. Push: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

## 📬 Contact & Support

- 📧 Email: your.email@example.com
- 🐛 Bug Reports: [Open an Issue](https://github.com/YourUsername/maize-yield-gap-analyser/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/YourUsername/maize-yield-gap-analyser/discussions)

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

---

<p align="center">
  <b>🌽 Maize Yield Gap Analyser</b><br>
  <i>Bridging the science of crop potential with the reality of the Indian farmer's field.</i><br><br>
  Free · No sign-up · Evidence-based · AI-powered · Built for India
</p>
