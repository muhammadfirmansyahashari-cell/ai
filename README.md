# Nusa AI

Chatbot AI berbasis transformer yang berjalan 100% di browser, memakai [Transformers.js](https://github.com/huggingface/transformers.js) dan model open-source yang sudah dilatih (pretrained). Tanpa server, tanpa API key.

## Cara upload ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `nusa-ai`.
2. Upload `index.html` dan `README.md` ke repository tersebut.
3. Buka **Settings → Pages**.
4. Pada **Source**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit. Situsmu aktif di `https://USERNAME.github.io/nusa-ai/`.

## Kustomisasi

- Nama dan tampilan: edit bagian `<style>` dan `<h1>` di `index.html`.
- Kepribadian AI: ubah konstanta `SYSTEM` di bagian script.
- Model: tambah `<option>` di dropdown dengan model ONNX dari [huggingface.co/onnx-community](https://huggingface.co/onnx-community).

## Catatan

- Model kecil (0,3–1,5 miliar parameter) jauh lebih terbatas dibanding Claude atau GPT. Cocok untuk belajar dan eksperimen.
- WebGPU (Chrome/Edge terbaru) membuat jawaban jauh lebih cepat. Tanpa WebGPU, model berjalan di CPU dan lebih lambat.
- Unduhan model terjadi sekali, lalu tersimpan di cache browser.

## Ide pengembangan berikutnya

- Render Markdown dan blok kode pada jawaban.
- Simpan riwayat chat di `localStorage`.
- Fine-tune model dengan data sendiri (LoRA) lalu konversi ke ONNX.
- Sambungkan ke API model besar lewat backend kecil (Cloudflare Workers atau Vercel) agar jawabannya sekelas Claude/GPT.
