# prompt-upgrade examples

Examples illustrate the decision process. They are not rigid templates.

## Example 1: Dashboard website

**Original prompt**

> buatkan saya website dashboard paling bagus

**Upgraded prompt**

> Buat sebuah website dashboard modern dan rapi dengan fokus pada kemudahan membaca informasi, navigasi yang jelas, dan hierarki visual yang kuat.
>
> **Scope**
> - Buat dashboard generik karena jenis data dan bidang pengguna belum ditentukan.
> - Gunakan tata letak yang responsif untuk desktop, tablet, dan ponsel.
> - Susun area utama dengan header, navigasi yang proporsional, ringkasan informasi, dan area konten yang mudah dipindai.
> - Gunakan data contoh yang jelas ditandai sebagai data dummy; jangan mengklaim data tersebut berasal dari layanan nyata.
> - Jaga konsistensi tipografi, jarak, warna, komponen, dan status interaksi.
>
> **Batasan**
> - Jangan menambahkan login, database, API eksternal, pembayaran, analitik, atau panel admin karena fitur-fitur tersebut belum diminta.
> - Jangan menambahkan fitur yang tidak membantu tujuan dashboard.
> - Jika teknologi tidak ditentukan, pilih pendekatan sederhana dan jelaskan pilihan tersebut secara singkat.
>
> **Deliverable**
> - Berikan implementasi lengkap yang dapat dijalankan, bukan hanya deskripsi desain.
> - Sertakan nama/path file dan instruksi menjalankan yang benar-benar diperlukan.
> - Periksa responsivitas, keterbacaan, dan interaksi utama sebelum menyatakan selesai.
> - Sebutkan dengan jujur bagian yang belum diimplementasikan atau belum dapat diuji.

**Why this works:** It makes “dashboard paling bagus” actionable without guessing the dashboard's industry or quietly imposing a backend.

**Possible optional suggestion:** If the user knows the dashboard's purpose, ask them to name it (for example, school activity, sales, or project tracking). Do not block the first draft if a generic dashboard is acceptable.

## Example 2: Simple school landing page

**Original prompt**

> buat landing page HTML sederhana untuk proyek sekolah

**Upgraded prompt**

> Buat landing page sederhana untuk proyek sekolah menggunakan HTML dan CSS, dengan struktur yang mudah dipahami dan gampang diedit oleh pelajar.
>
> Include a clear project title, a short introduction, the main project information, and a footer. Use readable typography, sensible spacing, and a responsive layout. Keep the visual design neat but do not overcomplicate it.
>
> Return the complete code and identify the files. Do not add JavaScript, a backend, a framework, accounts, or external services unless they are necessary and explicitly approved. Do not invent the school's name, project facts, or student details; use clearly marked placeholders where information is missing.

**Why this works:** It fills in deliverable and usability details without turning a simple school project into a production web app.

## Example 3: Image generation

**Original prompt**

> Gambar stasiun kereta Indonesia saat hujan malam, realistis.

**Upgraded prompt**

> Create a realistic image of an Indonesian railway station at night during steady rain. Show wet platform surfaces reflecting station lights, subtle rain in the air, and a believable Indonesian railway environment. Use a grounded photographic composition with natural perspective and realistic materials. Keep signs and text minimal and legible; do not invent a specific station name, railway logo, or identifiable real person. Prioritize a convincing rainy-night atmosphere over dramatic fantasy effects.

**Why this works:** Every addition strengthens the scene or prevents unsupported specificity. It does not add unrelated poster design or branding.

## Example 4: Don't over-edit

**Original prompt**

> Write a 100-word announcement in Indonesian that tomorrow's club meeting starts at 3 PM.

**Expected approach:** Keep the 100-word limit, Indonesian language, meeting date reference, and 3 PM time. If the club name and venue are absent, use placeholders or write around them. Do not invent the club name, venue, agenda, or new event details just to make the announcement sound complete.
