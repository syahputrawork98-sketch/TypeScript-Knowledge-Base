# TypeScript Knowledge Base: Total Deconstruction Plan

> **Status Spec-Sync**: v5.4 -> v5.7 (Alignment Path)
> **Last Updated**: 2026-03-19

Dokumen ini adalah cetak biru (blueprint) modular yang mendekomposisi **seluruh** dokumentasi resmi TypeScript ([typescriptlang.org/docs](https://www.typescriptlang.org/docs/)) ke dalam arsitektur **Source-Driven 8-Rack**. Desain ini ditingkatkan dari model 5-Rack awal untuk mencerminkan navigasi asli dokumentasi resmi, memastikan sinkronisasi yang lebih mudah dengan pembaruan rilis di masa depan.

---

## 🏗 Justifikasi Teknis (The Mirroring Principle)

Arsitektur ini didesain menggunakan pendekatan **True-Source Mirroring**. Kita tidak lagi memaksakan struktur eksternal, melainkan mengikuti cara tim inti TypeScript mengorganisir pengetahuan mereka.

### 1. RAK-01: Get Started (The Entry Points)
Fokus pada jalur onboarding spesifik berdasarkan latar belakang pengembang.
- **Justifikasi**: Meminimalkan "Time to Hello World" dengan tutorial yang dipersonalisasi.

### 2. RAK-02: The Handbook (The Narrative Core)
Jantung dari pembelajaran TypeScript, mencakup evolusi dari tipe dasar hingga manipulasi tipe yang kompleks.
- **Justifikasi**: Mengikuti progresi logis yang disarankan oleh tim TS untuk penguasaan bahasa.

### 3. RAK-03: Reference (Technical Deep Dives)
Detail teknis tentang mekanika internal bahasa dan fitur-fitur khusus.
- **Justifikasi**: Kamus operasional untuk aturan-aturan yang tidak dibahas secara naratif di Handbook.

### 4. RAK-04: Modules (The Complexity Layer)
Membedah teori dan implementasi modul di ekosistem JS modern (ESM vs CJS).
- **Justifikasi**: Modul adalah salah satu titik paling membingungkan di TS saat ini; pemisahan ke Rak khusus sangat kritikal.

### 5. RAK-05: Declaration Files (.d.ts Mastery)
Panduan lengkap untuk pembuatan, penggunaan, dan publikasi file deklarasi.
- **Justifikasi**: Krusial untuk pengembangan library dan interoperabilitas dengan library JS murni yang tidak memiliki tipe.

### 6. RAK-06: JavaScript Integration (The Bridge)
Bagaimana TS berinteraksi dengan codebase JS murni menggunakan JSDoc dan type checking eksternal.
- **Justifikasi**: Mendukung skenario migrasi bertahap dan penggunaan TS sebagai alat audit JS.

### 7. RAK-07: Project Configuration (The Engine)
Kontrol compiler, optimasi build, dan manajemen project reference.
- **Justifikasi**: Mengelola skalabilitas codebase besar melalui `tsconfig.json` dan strategi build.

### 8. RAK-08: Evolution & Releases (The Pulse)
Sejarah rilis dan roadmap fitur masa depan bahasa tersebut.
- **Justifikasi**: Memastikan *Knowledge Base* tetap relevan dengan mengikuti derap langkah TC39 dan Microsoft.

---

## 🗄 Peta Arsitektur Detail (Source Mapping)

| Rak | Sub-Rak (SR) | Buku (BK) | Deskripsi BK |
| :--- | :--- | :--- | :--- |
| **RAK-01** | **SR-01: Basics** | BK-01: Quickstart | Tutorial 5 menit & Tooling Intro. |
| | **SR-02: Backgrounds** | BK-01: New Programmers | Dasar bagi yang baru belajar koding. |
| | | BK-02: JS Programmers | Transisi dari Vanilla JavaScript. |
| | | BK-03: Java/C# Users | Structural vs Nominal comparison. |
| | | BK-04: Functional | Pendekatan FP di TypeScript. |
| **RAK-02** | **SR-01: Foundations** | BK-01: The Basics | Static types, Non-exception failures. |
| | | BK-02: Everyday Types | Primitives, Unions, Type Aliases. |
| | **SR-02: Logic** | BK-03: Narrowing | Control flow analysis & Type guards. |
| | | BK-04: Functions | Overloads, Generics, `this` types. |
| | | BK-05: Object Types | Shape definition & Index signatures. |
| | **SR-03: Manipulation**| BK-06: Type Manipulation | Generics, Conditional, Mapped Types. |
| | **SR-04: Structure** | BK-07: Classes | Visibility, Heritage, Static members. |
| | | BK-08: Modules | Import/Export syntax & Loading logic. |
| **RAK-03** | **SR-01: Types** | BK-01: Utility Types | Pick, Omit, Record, etc. |
| | | BK-02: Enums | Numeric vs String Enums. |
| | **SR-02: Mechanics** | BK-03: Compatibility | Subtyping rules & structural checks. |
| | | BK-04: Inference | Contextual & Best Common Type. |
| | **SR-03: Syntax** | BK-05: JSX | UI components & React support. |
| | | BK-06: Decorators | Experimental & Legacy Metadata. |
| **RAK-04** | **SR-01: Theory** | BK-01: Module Theory | History and why we have modules. |
| | **SR-02: Practical** | BK-02: ESM/CJS Interop | Managing `module` & `moduleResolution`. |
| **RAK-05** | **SR-01: Authoring** | BK-01: Library Structure | Declaration patterns for libraries. |
| | | BK-02: .d.ts Templates | Modular, Class, and Global templates. |
| | **SR-02: Advanced** | BK-03: Deep Dive | Do's and Don'ts of definitions. |
| **RAK-06** | **SR-01: JS Workflow** | BK-01: Type Checking JS | Using `allowJs` and `checkJs`. |
| | | BK-02: JSDoc Ref | Type representation in comments. |
| **RAK-07** | **SR-01: Config** | BK-01: tsconfig.json | Complete catalog of compiler options. |
| | **SR-02: Scale** | BK-02: Project Refs | Composite projects architecture. |
| **RAK-08** | **SR-01: Updates** | BK-01: Version Logs | Change logs from v1.0 to v5.x. |
| | **SR-02: Future** | BK-02: Stage Roadmap | Monitoring TC39 state. |

---

## 🛠 Protokol PPM V4 (Modified for Sync)

1.  **Direct Linking**: Setiap Bab (CH) dalam Buku WAJIB mencantumkan URL absolut dari documentation resmi sebagai "Anchor Source".
2.  **Structural Integrity**: Hierarki folder harus mengikuti `R[XX]/SR[XX]/BK[XX]`.
3.  **Modular Independence**: Buku di RAK-03 (Reference) tidak boleh bergantung pada narasi di RAK-02 (Handbook) agar bisa dibaca secara acak.

---

## 📜 Log Sinkronisasi (Spec-Log)

| Versi TS | Tanggal Audit | Perubahan Arsitektur/Konten | Status |
| :--- | :--- | :--- | :--- |
| **v5.4** | 2026-03-19 | Inisialisasi awal 5-Rack. | 🔄 Replaced |
| **v5.7** | 2026-03-19 | Migrasi ke 8-Rack (Source-Driven Model). | ✅ Synced |

---

## 📈 Prinsip Pengerjaan

1.  **Source First**: Jangan menulis konten jika sumber resminya belum terpetakan.
2.  **Breadcrumb Check**: Pastikan setiap file `README.md` di level sub-folder memiliki link kembali ke Master Plan ini.
3.  **Visual Evidence**: Setiap penambahan Buku baru wajib menyertakan diagram hubungan antarentitas tipe.
