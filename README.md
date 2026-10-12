# Kevin OS Model

**Kevin Open Source Model** — Kumpulan skill open source yang bisa dipakai di AI (Claude & Grok).

> Dibuat & di-maintain oleh **Kevin** (`@lausiapempruy`)

---

## Apa ini?

`kevin-os-model` adalah repository skill modular yang dirancang khusus agar bisa langsung dipakai di:

- **Claude** (via Projects / Custom Instructions / Artifacts)
- **Grok** (via system prompt / connector / custom tools)

Setiap skill berdiri sendiri, mudah di-copy, dan bisa digabung sesuai kebutuhan.

---

## Struktur Repository

```
kevin-os-model/
├── skills/                  # Semua skill disimpan di sini
│   └── (skill-name)/
│       ├── SKILL.md         # Instruksi utama skill
│       └── ...              # File pendukung (opsional)
├── assets/                  # Logo, icon, dll
├── LICENSE
├── CONTRIBUTING.md
└── README.md
```

---

## Cara Pakai

### Untuk Grok
1. Copy isi file `SKILL.md` dari skill yang diinginkan
2. Paste ke system prompt / custom instruction
3. Atau gunakan langsung lewat connector

### Untuk Claude
1. Buat Project baru di Claude
2. Upload atau paste isi `SKILL.md` sebagai Custom Instruction / Knowledge
3. Aktifkan skill sesuai kebutuhan

---

## Skill yang Tersedia

| Skill | Deskripsi | Status |
|-------|-----------|--------|
| *Coming soon* | - | - |

---

## Kontribusi

Mau nambah skill baru? Baca dulu [CONTRIBUTING.md](CONTRIBUTING.md).

Pull request sangat diterima!

---

## Lisensi

MIT License — bebas dipakai, dimodifikasi, dan didistribusikan.

---

**Kevin OS Model**  
Open Source Skills for the next generation of AI.