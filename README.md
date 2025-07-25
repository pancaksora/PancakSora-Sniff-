# 📡 PancakSora Sniff

**LoRa Packet Sniffer Firmware** for LilyGo T3 V1.6.1 + OLED

> Firmware ini mendeteksi, merekam, dan menampilkan semua aktivitas LoRa di udara secara real-time — cocok untuk debugging, eksplorasi sinyal, dan pembelajaran sistem mesh LoRa.  

---

## 🚀 Fitur
- ✅ Tangkap semua paket LoRa di frekuensi yang ditentukan
- 🛰️ Tampilkan data **RSSI**, **SNR**, dan **jumlah paket** di layar OLED 0.96"
- 🔍 Bisa digunakan untuk memonitor node Meshtastic, LoRaWAN, atau protokol custom lainnya
- ⚡ Dibuat khusus untuk board **LilyGo LoRa T3 V1.6.1** (ESP32 + SX1276 + OLED SSD1306)

---

## ⚙️ Konfigurasi LoRa

```cpp
LoRa.begin(915E6);             // Ganti sesuai region: 433E6 / 868E6 / 915E6
LoRa.setSpreadingFactor(7);    // SF7 = default, bisa disesuaikan (6–12)
LoRa.setSignalBandwidth(125E3);// 125kHz = default Meshtastic
LoRa.setCodingRate4(5);        // Coding rate 4/5
✅ Sesuaikan frekuensi dengan wilayahmu:
🇪🇺 868 MHz (Europe, Middle East)
🇺🇸 915 MHz (US, Saudi, Asia)
🇨🇳 433 MHz (beberapa negara)

📷 Tampilan OLED (Simulasi)
OLED akan menampilkan:
📦 Jumlah paket diterima
📶 Nilai RSSI dan SNR terakhir
🕵️ Status "LoRa Listening..."

📦 Persiapan
🧰 Hardware:
LilyGo LoRa T3 V1.6.1 (ESP32 + SX1276 + OLED)
USB-C Cable
(Opsional) Powerbank untuk operasi mobile

💻 Software:
Visual Studio Code + PlatformIO
Atau Arduino IDE (dengan beberapa penyesuaian)

📂 Instalasi & Upload
1. Clone repo ini: git clone https://github.com/pancaksora/pancaksora-sniff.git
2. Buka folder project di VS Code
3. Hubungkan board LilyGo ke komputer
4. Klik tombol “Upload” di PlatformIO
5. Buka Serial Monitor (115200 baud) untuk melihat log paket yang masuk
6. Cek OLED untuk tampilan real-time

🛡️ Catatan Penting
🔐 Sniffer ini tidak dapat membaca isi paket terenkripsi (seperti AES Meshtastic)
🎯 Tujuan utama adalah deteksi dan logging sinyal LoRa, bukan decoding payload
⚡ Firmware ini cocok untuk eksplorasi sinyal, debugging mesh, dan pengamatan frekuensi

🙌 Credits
Firmware ini dikembangkan oleh Ali Muhsi Kemal (PancakSora)
Sambil ngopi malam-malam ☕🤖
