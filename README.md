# Hybrid Chaos-PQC Image Encryption — IEEE Conference Paper

> **Hybrid Chaos-PQC Image Encryption: Post-Quantum Key Establishment via ML-KEM-768 with Dual Confusion–Dual Diffusion Chaotic Maps**

## Authors

| Name | Affiliation | Email |
|---|---|---|
| Hafas Furqan | Cryptographic Engineering, Politeknik Siber dan Sandi Negara | hafas.furqan@student.poltekssn.ac.id |
| Yeni Farida | Cryptographic Engineering, Politeknik Siber dan Sandi Negara | yeni.farida@poltekssn.ac.id |
| Andika Aryansyach Fauzan | Cryptographic Engineering, Politeknik Siber dan Sandi Negara | andika.aryansyach@student.poltekssn.ac.id |

## Paper Overview

This paper proposes a hybrid image encryption scheme combining:
- **ML-KEM-768** (FIPS 203) for post-quantum key establishment
- **HKDF-SHA-256** to derive 18 independent chaos parameters (144-byte OKM)
- **4-stage pipeline:** Lorenz Confusion → Logistic Diffusion → Lorenz Confusion → Tent Diffusion

Experiments on 9 grayscale images show mean entropy **7.9994 bits**, mean |correlation| **7×10⁻⁴**, and mean PSNR **7.79 dB**.

---

## Files in this Repository

| File | Description |
|---|---|
| `paper_hybrid_chaos_pqc.tex` | **Main LaTeX source** — edit this file |
| `IEEEtran.cls` | IEEE conference class file (required for compilation) |
| `paper_hybrid_chaos_pqc.pdf` | Latest compiled PDF |

---

## How to Compile Locally

### Requirements
- **MiKTeX** (Windows) atau **TeX Live** (Linux/Mac)
- Pastikan `pdflatex` tersedia di PATH

### Steps

```bash
# Clone repository
git clone https://github.com/0xAre/paper-hybrid-chaos-pqc.git
cd paper-hybrid-chaos-pqc

# Compile (2x untuk resolve cross-references)
pdflatex paper_hybrid_chaos_pqc.tex
pdflatex paper_hybrid_chaos_pqc.tex
```

Output: `paper_hybrid_chaos_pqc.pdf`

### Dengan Overleaf (tanpa install apapun)
1. Download semua file dari repo ini sebagai ZIP
2. Buka [overleaf.com](https://overleaf.com) → **New Project** → **Upload Project**
3. Upload ZIP → langsung bisa edit dan compile di browser

---

## How to Contribute / Edit

### 1. Clone repo
```bash
git clone https://github.com/0xAre/paper-hybrid-chaos-pqc.git
cd paper-hybrid-chaos-pqc
```

### 2. Edit file LaTeX
Buka `paper_hybrid_chaos_pqc.tex` dengan editor LaTeX pilihanmu:
- **VS Code** + LaTeX Workshop extension
- **TeXstudio**
- **Overleaf** (upload manual)

### 3. Struktur section di file `.tex`

| Section | Baris awal | Deskripsi |
|---|---|---|
| Abstract | `\begin{abstract}` | Ringkasan paper |
| Section I | `\section{Introduction}` | Latar belakang |
| Section II | `\section{Background}` | Teori & related work |
| Section III | `\section{Proposed Hybrid...}` | Skema yang diusulkan |
| Section IV | `\section{Experimental Results}` | Hasil eksperimen |
| Section V | `\section{Discussion}` | Pembahasan |
| Section VI | `\section{Conclusion}` | Kesimpulan |
| References | `\begin{thebibliography}` | Daftar pustaka |

### 4. Commit dan push perubahan
```bash
git add paper_hybrid_chaos_pqc.tex
git commit -m "section: deskripsi singkat perubahan"
git push origin main
```

**Contoh pesan commit yang baik:**
```
fix: perbaiki sitasi b19 di section II
edit: tambah analisis histogram section IV
update: revisi abstract
```

### 5. Update PDF setelah edit
Setelah compile ulang, update PDF di repo:
```bash
git add paper_hybrid_chaos_pqc.pdf
git commit -m "pdf: update compiled PDF"
git push origin main
```

---

## Citation

Jika paper ini dipublikasikan, silakan cite:

```bibtex
@inproceedings{furqan2025hybridchaospqc,
  title     = {Hybrid Chaos-PQC Image Encryption: Post-Quantum Key Establishment via ML-KEM-768 with Dual Confusion--Dual Diffusion Chaotic Maps},
  author    = {Furqan, Hafas and Farida, Yeni and Fauzan, Andika Aryansyach},
  booktitle = {IEEE Conference Proceedings},
  year      = {2025},
  institution = {Politeknik Siber dan Sandi Negara}
}
```
