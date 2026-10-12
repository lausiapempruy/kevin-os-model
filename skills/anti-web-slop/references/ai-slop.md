# AI Slop Checklist (50 points)

Use this when auditing or building any web UI, landing page, dashboard, or app interface. Flag and rewrite any matching pattern.

## Bagian 1: Visual, Layout, dan Branding (1-15)

1. **Gradient biru-ungu khas AI**  
   Kombinasi gradient biru → ungu/violet yang dominan di header, background, atau kartu (pola default v0 & bolt.new).

2. **Dark mode neon glow + ambient light blob**  
   Background gelap (slate-900/black) + bulatan cahaya neon pudar + border kartu transparan berpendar (backdrop-blur).

3. **Bento grid yang dipaksa**  
   Layout bento grid asimetris dipasang di semua tempat, termasuk konten linier/sederhana.

4. **Badge kecil di atas hero**  
   Badge kapsul kecil berpendar tepat di atas judul utama ("// now in beta", "⚡ ai-powered", "v2.0 released").

5. **Logo text-only tanpa brand identity**  
   Logo hanya teks sans-serif polos tanpa simbol, grafis, atau tipografi khas.

6. **No favicon / favicon default framework**  
   Tab browser masih menampilkan logo Vercel, Next.js, Vite, atau ikon globe bawaan.

7. **Hero text gradient / animasi ganti warna**  
   Judul utama pakai text-transparent bg-clip-text gradient atau tulisan berganti warna tidak alami.

8. **Font cursive/handwriting pada kata penekanan**  
   Font tulisan tangan untuk 1-2 kata di tengah judul utama demi kesan "human touch" generik.

9. **Emoji icons menggantikan vector icons**  
   Emoji standar (🚀 💡 ⚡) sebagai ikon fitur, bukan ikon vektor konsisten (Lucide, Heroicons, custom).

10. **Komponen shadcn/ui polos tanpa kustomisasi**  
    Button, dialog, card, dropdown 100% styling bawaan shadcn/Radix warna zinc/slate.

11. **Gambar & ilustrasi AI slop (over-polished / uncanny)**  
    Visual produk atau dekoratif dari AI generate yang objeknya tidak nyata, proporsi aneh, atau terlalu mengkilap.

12. **Avatar stack dengan foto Unsplash/AI**  
    Deretan foto profil bertumpuk ("+1,000 happy users") pakai foto stok atau avatar AI terlalu sempurna.

13. **Scroll animations & entrance effect berlebihan**  
    Setiap elemen melayang naik (framer-motion y:20→0) dengan spring berat yang lambat di perangkat spek rendah.

14. **One-page website tanpa hierarki navigasi**  
    Seluruh informasi dipaksakan dalam 1 halaman panjang tanpa sub-halaman (About, Docs, Blog).

15. **Watermark / tag tool AI generator**  
    Masih ada badge "edit with lovable", "built with v0", "made with bolt.new".

## Bagian 2: Copywriting dan Konten (16-25)

16. **Em dash (—) berlebihan**  
    Kalimat sering memakai tanda hubung panjang untuk menyambung klausa (ciri khas struktur AI).

17. **Vague hero copywriting**  
    Judul puitis tanpa menjelaskan produk ("empowering intelligent workflows for the next generation").

18. **Buzzword bingo**  
    "seamlessly integrate", "revolutionize your workflow", "leverage cutting-edge intelligence", "elevate your productivity".

19. **Fake reviews & testimonial fiktif**  
    Nama fiktif + foto stok + kutipan puitis yang jelas bukan dari manusia asli.

20. **Fake metrics & klaim statistik tidak valid**  
    "99.9% accuracy", "10x faster", "500+ integrations" tanpa bukti atau data pendukung.

21. **Fake customer count / user counter**  
    "Join 12,847+ creators" dengan angka stasis atau palsu.

22. **Badge tech stack mencolok di hero (produk non-dev)**  
    Menampilkan Next.js, Tailwind, Supabase, OpenAI di halaman depan untuk audience B2C non-teknis.

23. **Code snippet dekoratif tidak berfungsi**  
    Blok kode berpendar di landing page hanya untuk gaya (produk bukan dev tool).

24. **Pricing 3 kolom standar kaku**  
    Starter / Pro (badge Most Popular) / Enterprise dengan daftar centang hijau yang berulang.

25. **Tidak ada halaman legal valid**  
    Privacy Policy & Terms of Service mengarah ke 404, kosong, atau placeholder generik.

## Bagian 3: Fungsionalitas, UX & Teknis (26-38)

26. **Domain gratisan vercel.app / netlify.app**  
    Masih pakai subdomain hosting gratis tanpa custom domain resmi.

27. **Tampilan mobile berantakan**  
    Elemen tumpang tindih, teks terpotong, atau horizontal scrollbar di HP.

28. **Broken buttons & unhandled click**  
    Tombol utama tidak merespons atau hanya `href="#"`.

29. **Fake live visitor counter**  
    Widget "🟢 232 people online" dengan angka hardcode atau Math.random().

30. **Fake toast notifications**  
    "John from NY just purchased Pro Plan!" yang looping berdasarkan timer.

31. **Form submit palsu**  
    Form tanpa backend: isi kosong lalu langsung sukses, atau hanya toast "Coming Soon!".

32. **Dummy authentication & localStorage mock**  
    Login tidak ke server asli, langsung dashboard dengan mock user di localStorage.

33. **OpenGraph metadata tidak diatur**  
    Preview di WhatsApp/Discord/X kosong atau masih logo bawaan Vercel/Next.js.

34. **Blinking green dot status palsu**  
    Titik hijau animate-ping + "System Operational" tanpa health check nyata.

35. **Logo marquee perusahaan fiktif**  
    Infinite slider logo Acme Corp, Globex, Stark Ind atau SVG acak tanpa kerjasama riil.

36. **Performa lambat (oversized assets)**  
    Bundle besar karena library animasi berlebihan, banyak font, gambar AI tanpa WebP.

37. **Tidak ada error state / loading skeleton**  
    Saat error: blank putih, console error, atau tidak ada skeleton rapi.

38. **Link footer mati / tidak ada kontak resmi**  
    About, Careers, Blog, Contact tidak aktif; tidak ada email atau alamat valid.

## Bagian 4: Detail Mikroskopis & Nuansa (39-50)

39. **Glassmorphism berlebihan**  
    Hampir semua panel/navbar/popup pakai backdrop-blur hingga teks di belakang sulit dibaca.

40. **Gradasi teks kontras rendah (accessibility fail)**  
    Teks kecil abu-abu muda (text-zinc-500) di background gelap, gagal WCAG.

41. **Custom cursor melayang yang lag**  
    Kursor lingkaran berbuntut animasi yang delay saat mouse bergerak.

42. **Noise texture background dipaksa**  
    Grainy overlay opacity tinggi yang membuat layar terlihat kotor.

43. **Struktur heading HTML acak**  
    Skip level (h1 langsung ke h4) hanya karena ukuran font, bukan hierarki SEO/a11y.

44. **Marquee text kalimat panjang kencang**  
    Running text promosi bergerak terlalu cepat, sulit dibaca.

45. **Glow border form input saat fokus**  
    Input mengeluarkan pendaran neon terlalu lebar hingga menutupi label.

46. **Hyphenation / line wrap janggal**  
    Judul terpotong di tengah kata tanpa text-wrap: balance.

47. **Ilustrasi Corporate Memphis / 3D clay AI**  
    Karakter 3D tanah liat atau kartun bertangan besar khas generatif AI 2023.

48. **Tidak ada state hover/active jelas**  
    Tombol/kartu tidak berubah warna, scale, atau feedback visual saat di-hover.

49. **Dark/light mode toggle tidak berfungsi baik**  
    Hanya satu mode, atau switch merusak tampilan/warna teks.

50. **Ketergantungan total pada CDN eksternal tanpa fallback**  
    Gambar/ikon/script dari CDN gratis atau domain sementara AI tanpa local/S3.