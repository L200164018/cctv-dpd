# CCTV Live Web Monitor (Vercel Edition) 🌐

Aplikasi web surveillance CCTV modern yang siap di-deploy ke **Vercel** dan diakses dari mana saja (Desktop, Laptop, Tablet, Smartphone) via browser.

---

## 🚀 Cara Deploy ke Vercel (1 Menit)

1. Buka [Vercel Dashboard](https://vercel.com/new).
2. Klik **"Add New Project"** lalu pilih repositori GitHub ini.
3. Klik **"Deploy"** (tanpa perlu ubah pengaturan build).
4. Selesai! Web Anda akan aktif di alamat seperti `https://cctv-web-monitor.vercel.app`.

---

## 🔌 Cara Menghubungkan CCTV Lokal ke Web Vercel

Karena CCTV Anda berada di jaringan lokal Wi-Fi (`rtsp://15.15.100.187:554/...`), sedangkan Vercel berada di Cloud publik (HTTPS), dibutuhkan jalur jembatan aman (*tunnel*) agar video bisa mengalir ke Vercel:

### Opsi Praktis: Cloudflare Quick Tunnel (100% Gratis & Tanpa Buka Port Router)
1. Jalankan streaming gateway di komputer yang terhubung ke Wi-Fi CCTV.
2. Buka tunnel dengan Cloudflare:
   ```bash
   cloudflared tunnel --url http://localhost:8889
   ```
3. Anda akan mendapatkan URL HTTPS publik, contoh:
   `https://cctv-live-abc123.trycloudflare.com`
4. Buka website Vercel Anda, tempelkan URL tersebut ke kolom **"Stream Gateway"**, lalu klik **Simpan & Hubungkan**.
5. CCTV langsung tayang di Vercel secara *real-time*!

---

## ✨ Fitur-Fitur
- ⚡ **WebRTC WHEP Streaming**: Latensi ultra-rendah (< 300 ms).
- 🔄 **HLS Fallback**: Kompatibel di semua browser (Chrome, Safari iOS, Edge, Firefox, Android).
- 📹 **Multi-Channel**: Beralih mudah antara Cam 10 (Main/Sub), Cam 1, Cam 2.
- 📸 **Snapshot**: Ambil foto rekaman resolusi penuh dalam format PNG.
- ⛶ **Fullscreen**: Mode monitor keamanan layar penuh.
- 📱 **Mobile Friendly**: Tampilan responsif di HP dan PC.
