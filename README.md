# BIG SpO₂ Monitor

**Bengal Institute of Gastroenterology — Camera-based Pulse Oximetry**

> Dr. Saptarshi Bishnu MD DM Hepatology · BIG, Bardhaman, West Bengal

---

## Live Demo

**[▶ Open App](https://saptarshibishnu.github.io/big-spo2/)**

> Replace `saptarshibishnu` with your actual GitHub username after upload.

---

## What It Does

A single-file, zero-dependency browser app that estimates **SpO₂ and Heart Rate** from the smartphone rear camera using the **PPG (Photoplethysmography)** method — the same optical principle used in clinical pulse oximeters.

### Algorithm

| Step | Detail |
|---|---|
| **Signal acquisition** | Camera frames captured at ~30 fps; 16×16 central pixel ROI averaged |
| **AC component** | Peak − trough of pulsatile signal (per 60-sample window) |
| **DC component** | Rolling mean (baseline offset) |
| **R-ratio** | `(AC_red/DC_red) ÷ (AC_green/DC_green)` — Red/Green proxy for clinical Red/IR |
| **SpO₂ estimate** | `SpO₂ ≈ 110 − 25 × R` (Beer-Lambert empirical calibration curve) |
| **Heart Rate** | Peak-to-peak interval of red-channel PPG waveform |
| **Perfusion Index** | `AC/DC × 100%` |

### Features

- 📡 Live PPG waveform with peak detection markers
- 🔵 SpO₂ circular ring with colour-coded thresholds (≥95% cyan · 90–94% yellow · <90% red)
- ❤️ Heart rate from peak-interval analysis
- 📊 Perfusion Index & R-ratio display
- 🔦 Torch/flashlight toggle (required for finger occlusion method)
- 🟩 Signal quality bar
- 🩺 Clinical interpretation (normal / mild / moderate / severe hypoxaemia grading)
- 📋 Reading history log with timestamps
- 📱 Mobile-first, offline-capable — no server, no backend

---

## How to Use

1. Open the app on a **smartphone browser** (Chrome on Android recommended)
2. Tap **Torch ON** to enable the flashlight
3. Place your **fingertip firmly** over the rear camera lens
4. Tap **▶ Start**
5. Hold still for **15–20 seconds** — readings stabilise after warm-up

---

## Deployment (GitHub Pages)

```bash
# 1. Create a new repo named:  big-spo2
# 2. Upload index.html and README.md
# 3. Go to Settings → Pages → Source: main branch / root
# 4. App will be live at: https://<your-username>.github.io/big-spo2/
```

---

## ⚠️ Disclaimer

This is a **research and educational prototype only**.

- Consumer smartphone cameras are **not spectrally calibrated** for medical oximetry
- Accuracy depends on torch quality, skin tone, contact pressure, and motion
- The Red/Green proxy is **not equivalent** to certified Red/IR pulse oximetry
- **Not validated for clinical decision-making**
- Always confirm with a **certified pulse oximeter** for medical purposes

---

## Citation / Acknowledgement

If used in research or education, please acknowledge:

> *BIG SpO₂ Monitor — Camera PPG prototype. Bengal Institute of Gastroenterology, Bardhaman. Dr. Saptarshi Bishnu MD DM Hepatology, 2026.*

---

## Related BIG Projects

- [BIG Endoscopy Suite](https://github.com/saptarshibishnu/big-endoscopy)
- [BodyScan Obesity Screening](https://github.com/saptarshibishnu/bodyanalysis)
- [LiverTransplant Analyzer (LTA)](https://github.com/saptarshibishnu/lta)

---

*Bengal Institute of Gastroenterology · Bardhaman, West Bengal, India*
