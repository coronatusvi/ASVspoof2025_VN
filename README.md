# VoiceSpoof-VN: Vietnamese Spoofed and Bonafide Speech Dataset

VoiceSpoof-VN is a publicly available dataset for research on speaker verification and spoofing countermeasures in Vietnamese. It contains over **71,000 utterances** from **262 speakers** across diverse acoustic and spoofing conditions. The dataset is designed to support research on **spoof detection**, **speaker verification**, and **language-specific vulnerabilities** in Vietnamese speech processing.

<p align="center">
  <img src="https://raw.githubusercontent.com/coronatusvi/ASVspoof2025_VN/refs/heads/master/access/F1.png" width="700"/>
</p>

---

## 🧪 Spoofing Types and Descriptions

| Code | Type   | Methodology Description | Vocoder/Technique | Transformation |
|------|--------|--------------------------|-------------------|----------------|
| A01  | Text + Speed | LLM + Flow + HIFT TTS synthesis | HiFi-GAN | None |
| A02  | Speed | WORLD vocoder with reverb and light pitch shift | WORLD | Reverb + pitch shift |
| A03  | Speed | Griffin-Lim vocoder with increased iterations | Griffin-Lim | None |
| A04  | Speech | Non-parallel VC using VAE preserving speaker timbre | VAE-based VC | None |
| A05  | Speech | LPCC+GMM filtering | Residual + LPC vocoder | Spectral filtering + OLA |
| A06  | Speech | Signal-based VC (pitch/speed alteration) | Signal-based VC | Transform-based |
| A07  | Text | VietTTS + pitch transformation | HiFi-GAN | None |
| A08  | Text | Adversarial: noise + reverb + compression | Adversarial-style spoof | Normalize + spectral subtraction |
| A09  | Speech | HiFi-GAN TTS + VC (speed & pitch) | HiFi-GAN + VC | Speed-up + pitch shift |
| A10  | Speech | Spectral filtering with LPC + 5kHz cutoff | Residual + LPC vocoder | High-frequency filtering |

---

## 🔎 Application Context

Rather than being a standalone corpus, this dataset was designed to **fit into a modern speaker verification pipeline**. As illustrated in the figure above:

1. A voice signal (genuine or spoofed) is captured from Vietnamese speakers.
2. It is passed to both:
   - a **Countermeasure (CM)** system for spoof detection
   - and an **Automatic Speaker Verification (ASV)** system for identity verification.
3. Each module outputs a score, and a joint decision is made to accept or reject the speaker.

This design enables more realistic evaluations of spoofing attacks, specifically for **Vietnamese speech**, and facilitates research on **robust, language-aware defenses**.

---

## 📥 Download

👉 **Dataset available via Google Drive**: [Download VoiceSpoof-VN](https://drive.google.com/file/d/1zAfQzzxQjEDHGkgW2t3SIW1Ink09QroH/view?usp=drive_link)  
(*Please cite this dataset if used in academic publications.*)

---

## 📄 License

This dataset is provided **for academic and non-commercial research only**. Please contact the author for commercial licensing inquiries.

---

## 📣 Citation
```bibtex
@misc{voicespoofvn2025,
  title        = {VoiceSpoof-VN: A Vietnamese Dataset for Spoofing and Speaker Verification Research},
  author       = {Anh H. Pham, Quang D. Vi, An Dang},
  year         = {2025},
  note         = {Dataset accessed July 2025}
}
