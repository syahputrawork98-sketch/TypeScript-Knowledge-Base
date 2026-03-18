# TypeScript Knowledge Base: Total Deconstruction Plan

> **Status Spec-Sync**: v5.4 (Last Checked: 2026-03-19)

Dokumen ini adalah cetak biru (blueprint) modular yang mendekomposisi **seluruh** dokumentasi resmi TypeScript ([typescriptlang.org/docs](https://www.typescriptlang.org/docs/)) ke dalam arsitektur 5-Rack. Desain ini dibuat agar mudah diperbarui seiring perkembangan rilis TypeScript yang sangat aktif (setiap ~3 bulan).

---

## 🏗 Justifikasi Teknis (The 5-Rack Logic)

Arsitektur ini didesain berdasarkan **filosofi teknis TypeScript** yang berfokus pada *structural typing*, *type erasure*, dan integrasi mendalam dengan ekosistem JavaScript modern.

### 1. RAK-01: Setup & Onboarding (The Zero-Entry Barrier)
- **Justifikasi**: TypeScript seringkali dianggap sulit dikonfigurasi bagi pemula. Rak ini fokus pada "Get Productive Fast" dengan menyediakan jalur khusus berdasarkan latar belakang pengembang (JS, Java, C#, atau Functional). Ini memastikan hambatan masuk minimal sebelum menyentuh logika tipe yang lebih dalam.
- **Sub-Rak (SR)**: Dibagi menjadi 2 (Getting Started & Tutorials) untuk memisahkan antara landasan teoretis peran-spesifik dan implementasi praktis (Migration/Tooling).

### 2. RAK-02: The Handbook (The Narrative Core)
- **Justifikasi**: Handbook adalah jantung dari narasi TypeScript. Berbeda dengan bahasa nominal, TS mengandalkan **Structural Typing**. Rak ini membedah progresi logis dari tipe dasar, logika gabungan (Functions/Objects), hingga mekanisme pembuatan tipe yang canggih (Generics/Advanced Mechanics).
- **Sub-Rak (SR)**: Terbagi menjadi 4 (Foundations, Compound Logic, Type Creation, Structure) yang mencerminkan anatomi bahasa dari level atomik hingga skala modular.

### 3. RAK-03: Reference (The Deep Dives)
- **Justifikasi**: TS memiliki banyak fitur khusus yang tidak ada di JS (Utility Types, Enums) dan fitur meta-programming (Decorators). Rak ini berisi dokumentasi mendalam tentang mekanisme internal compiler dan aturan kompatibilitas tipe yang kritikal bagi pengembang framework dan library.
- **Sub-Rak (SR)**: Dibagi menjadi 3 (Internals, Compatibility, Specialized Syntax) untuk memisahkan alat bantu koding, aturan logika compiler, dan sintaksis khusus (JSX/Namespaces).

### 4. RAK-04: Engineering & Tools (The Brain)
- **Justifikasi**: "Scalable JavaScript" membutuhkan kontrol compiler yang presisi. Rak ini membedah `tsconfig.json`, `tsc` API, dan strategi skalabilitas seperti *Project References*. Di sini, kita memperlakukan TS sebagai platform rekayasa, bukan sekadar transpiler.
- **Sub-Rak (SR)**: Dibagi menjadi 2 (Compiler Control & Ecosystem Engineering) untuk memisahkan eksekusi build dan manajemen infrastruktur tipe (`.d.ts`).

### 5. RAK-05: Ecosystem & Evolutions (The Allies)
- **Justifikasi**: TypeScript berkembang jauh lebih cepat daripada standar ECMAScript. Rak ini memastikan *Knowledge Base* tetap relevan dengan melacak perubahan besar di setiap rilis minor dan memetakan roadmap masa depan bahasa tersebut.
- **Sub-Rak (SR)**: Dibagi menjadi 2 (Release Logs & Future Standards) untuk memisahkan sejarah stabil dengan fitur-fitur eksperimental (Stages).

---

## 🗄 Peta Arsitektur Detail

| Rak | Sub-Rak | Buku (BK) | Deskripsi Singkat BK |
| :--- | :--- | :--- | :--- |
| **RAK-01** | SR-01 | BK-01: New Programmers | Dasar bahasa untuk pemula total. |
| | | BK-02: JS Programmers | Transisi bagi yang sudah paham vanilla JS. |
| | | BK-03: Java/C# | Structural vs Nominal typing. |
| | | BK-04: Functional | Pendekatan fungsional di TypeScript. |
| | SR-02 | BK-01: Quickstart | Tutorial 5 menit & aplikasi sederhana. |
| | | BK-02: Migration | Strategi de-JSDoc-ing & konversi file. |
| | | BK-03: Tooling Intro | Gulp, Webpack, & DOM Manipulation. |
| **RAK-02** | SR-01 | BK-01: The Basics | Dinamika statis & compiler checks. |
| | | BK-02: Everyday Types | Primitives, Unions, Aliases vs Interfaces. |
| | | BK-03: Narrowing | Guarding logic & flow analysis. |
| | SR-02 | BK-01: Functions | Overloads & Generic functions. |
| | | BK-02: Object Types | Shape definition & index signatures. |
| | SR-03 | BK-01: Generics | Reusable blueprint & constraints. |
| | | BK-02: Type Creation | `keyof`, `typeof`, & Indexed access types. |
| | | BK-03: Advanced | Conditional & Mapped Types. |
| | | BK-04: Templates | Template Literal Types. |
| | SR-04 | BK-01: Classes | Member visibility & Heritage. |
| | | BK-02: Modules | Syntax import/export & loading strategy. |
| **RAK-03** | SR-01 | BK-01: Utility Types | Katalog lengkap (Pick, Omit, etc). |
| | | BK-02: Enums | Numeric, String, & Constant Enums. |
| | | BK-03: Meta-Prog | Decorators & Mixins. |
| | SR-02 | BK-01: Compatibility | Subtyping mechanics & shape checking. |
| | | BK-02: Inference | Contextual typing & inference rules. |
| | SR-03 | BK-01: JSX | React support & UI templates. |
| | | BK-02: Specialized | Triple-Slash & Namespaces. |
| **RAK-04** | SR-01 | BK-01: tsc API | Compiler CLI & options. |
| | | BK-02: TSConfig | Deep dive strictly, modules, projects. |
| | SR-02 | BK-01: Declaration | Managing `.d.ts` files. |
| | | BK-02: Project Refs | Scalability with modular compiler. |
| | | BK-03: Type Testing | tsd, vitest/jest integration. |
| **RAK-05** | SR-01 | BK-01: Release Logs | Sejarah evolusi (V2 ke V5). |
| | | BK-02: Future Specs | Roadmap Companion (Stage 1-4). |

---

## 🔄 Protokol Sinkronisasi (Quarterly Sync Rule)

Mengingat rilis TypeScript yang sangat agresif (rata-rata setiap 3 bulan), repository plan ini wajib mengikuti protokol pembaruan berikut:

1.  **Iterative Audit**: Setiap rilis `vX.Y`, `repository-plan` harus diaudit terhadap [Official TS Release Notes](https://www.typescriptlang.org/docs/handbook/release-notes/overview.html).
2.  **Refactor Minimal**: Masukkan fitur baru ke dalam Rak/Buku yang ada jika memungkinkan, atau buat Buku baru dalam SR-01/02 di RAK-05 sebagai "Incubator" sebelum dipindah ke inti Handbook.
3.  **Spec Logging**: Perubahan wajib dicatat dalam Log Sinkronisasi di bawah ini.

---

## 📜 Log Sinkronisasi (Spec-Log)

| Versi TS | Tanggal Audit | Perubahan Arsitektur/Konten | Status |
| :--- | :--- | :--- | :--- |
| **v5.4** | 2026-03-19 | Inisialisasi awal 5-Rack & Justifikasi Teknis. | ✅ Synced |
| *v5.5* | *TBD* | *Antisipasi rilis berikutnya...* | ⚪ Planned |

---

## 📈 Prinsip Pengerjaan "Tanpa Setengah-setengah"

1.  **Iterasi Bottom-Up**: Mulai dari Bab (CH) terkecil, selesaikan 3 Tahap PPM V4.
2.  **Referensial**: Setiap Bab WAJIB mencantumkan sumber URL dokumentasi resmi di baris pertama.
3.  **Visual Sentris**: Jangan biarkan ada Buku tanpa diagram "The Transformer" di level Rak.
4.  **Continuous Sync**: Selalu periksa Log Sinkronisasi sebelum memulai pengerjaan Bab baru.
