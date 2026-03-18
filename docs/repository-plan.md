# TypeScript Knowledge Base: Total Deconstruction Plan

Dokumen ini adalah cetak biru (blueprint) lengkap yang mendekomposisi **seluruh** dokumentasi resmi TypeScript ([typescriptlang.org/docs](https://www.typescriptlang.org/docs/)) menjadi unit belajar modular.

---

## 🗄 Peta Hierarki Total (The 5-Rack Blueprint)

### RAK-01: Setup & Onboarding (The Gateway)
*Sumber: Get Started & Tutorials Hub*

- **SR-01: Getting Started (Role-Based)**
    - **BK-01: TS for New Programmers**: Dasar bahasa untuk pemula total.
    - **BK-02: TS for JS Programmers**: Transisi bagi yang sudah paham vanilla JS.
    - **BK-03: TS for Java/C# Programmers**: Memahami perbedaan Structural vs Nominal typing.
    - **BK-04: TS for Functional Programmers**: Pendekatan fungsional di TypeScript.
- **SR-02: Implementation Tutorials**
    - **BK-01: TS in 5 Minutes**: Quickstart untuk aplikasi web sederhana.
    - **BK-02: ASP.NET Core with TS**: Integrasi ke ekosistem .NET.
    - **BK-03: Gulp & Webpack Integration**: Automasi build process.
    - **BK-04: DOM Manipulation**: Berinteraksi dengan elemen HTML secara aman.
    - **BK-05: Migrating from JavaScript**: Strategi de-JSDoc-ing dan konversi file.

### RAK-02: The Handbook (The Narrative Core)
*Sumber: Handbook V2 (Acuan utama pembelajaran terstruktur)*

- **SR-01: Foundations**
    - **BK-01: The Basics**: Dinamika statis, compiler checks, dan tipe eksplisit.
    - **BK-02: Everyday Types**: Primitive, Any, Union, Literal Types, Alias vs Interface.
    - **BK-03: Narrowing**: Guarding logic, Truthiness, flow analysis.
- **SR-02: Compound Logic**
    - **BK-01: More on Functions**: Overloads, Generic functions, callbacks.
    - **BK-02: Object Types**: Shape definition, index signatures, optionality.
- **SR-03: Type Creation (Creating Types from Types)**
    - **BK-01: Generics**: Reusable blueprint & constraints.
    - **BK-02: Type Operators**: `keyof` dan `typeof` mechanics.
    - **BK-03: Data Access Types**: Indexed access types.
    - **BK-04: Advanced Mechanics**: Conditional Types & Mapped Types.
    - **BK-05: String Manipulation**: Template Literal Types.
- **SR-04: Structure**
    - **BK-01: Classes**: Membervisibility, Heritage, dan Static members.
    - **BK-02: Modules**: Syntax import/export dan strategi pemuatan modul.

### RAK-03: Reference (The Deep Dives)
*Sumber: Reference section (Materi spesifik dan mendalam)*

- **SR-01: Language Internals**
    - **BK-01: Utility Types**: Katalog lengkap (Pick, Omit, Exclude, dsb).
    - **BK-02: Enums**: Numeric, String, dan Constant Enums.
    - **BK-03: Meta-Programming**: Decorators (PPM Stage 3) dan Mixins.
    - **BK-04: Iterators & Generators**: Protokol iterasi di TS.
- **SR-02: Type Logic & Compatibility**
    - **BK-01: Type Compatibility**: Mekanisme subtyping dan pengecekan bentuk.
    - **BK-02: Type Inference**: Cara compiler menebak tipe (contextual typing).
    - **BK-03: Symbols**: Penggunaan tipe unik di TS.
- **SR-03: Specialized Syntax**
    - **BK-01: JSX**: Dukungan React dan template UI.
    - **BK-02: Triple-Slash Directives**: Instruksi compiler di dalam file.
    - **BK-03: Namespaces**: Pengelolaan ruang lingkup (Legacy vs Modern).

### RAK-04: Engineering & Tools (The Brain)
*Sumber: Tools section & TSConfig Reference*

- **SR-01: Compiler Control**
    - **BK-01: tsc API & CLI**: Penggunaan compiler via terminal.
    - **BK-02: TSConfig Master Class**: Bedah seluruh kategori konfigurasi (Strictness, Modules, Projects).
- **SR-02: Ecosystem Engineering**
    - **BK-01: Declaration Files**: Menulis dan mengelola file `.d.ts`.
    - **BK-02: Project References**: Skalabilitas repositori besar dengan modularisasi compiler.
    - **BK-03: Testing Frameworks**: Type testing (tsd, vitest/jest integration).

### RAK-05: Evolutions (The Allies)
*Sumber: What's New & Blog*

- **SR-01: Release Logs**
    - **BK-01: Evolution Overview**: Sejarah perubahan besar (V2 ke V5).
    - **BK-02: Current Release Log**: Detail fitur versi terbaru (TS 5.x).
- **SR-02: Future & Standards**
    - **BK-01: Roadmap Companion**: Fitur-fitur yang sedang direncanakan (Stage 1-4).

---

## 📈 Prinsip Pengerjaan "Tanpa Setengah-setengah"
1.  **Iterasi Bottom-Up**: Mulai dari Bab (CH) terkecil, selesaikan 3 Tahap PPM V4.
2.  **Referensial**: Setiap Bab WAJIB mencantumkan sumber URL dokumentasi resmi di baris pertama.
3.  **Visual Sentris**: Jangan biarkan ada Buku tanpa diagram "The Transformer" di level Rak.
