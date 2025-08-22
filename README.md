# Incorrect-Hashing-MD5-in-Many-AI-Chatbots
Bug Report: Incorrect Hashing (MD5) in Many AI Chatbots

# ⚠️ Bug Report: Incorrect Hashing (MD5) in Many AI Chatbots

## Bug Description
I discovered a common bug in many AI chatbots when asked to generate a **hash value (e.g., MD5)** for a given string.  

Example case:  

**User input:**  

What is the MD5 of: admin1

**Chatbot answer (incorrect):**  

The MD5 of "admin1" is: 7c4a8d09ca3762af61e59520943dc264


However, the **correct MD5** of `admin1` is:  

e00cf25ad42683b3df678c61f42c6bda

## Impact
- **Confuses users**: Anyone relying on the chatbot for accurate hashing will receive incorrect information.  
- **Potentially dangerous in real-world applications**: Hashes are often used in security (passwords, file verification, etc.). Wrong results could lead to vulnerabilities or system errors.  

## Possible Cause
Most likely, the chatbot does not actually compute the hash, but instead "hallucinates" or guesses based on patterns in training data.  

## Recommendations for Chatbot Developers
1. **Do not rely on the model to compute hashes** – use official programming libraries (e.g., `hashlib` in Python).  
2. **Always validate results** using standard hashing functions before returning them to the user.  
3. **Add a fallback mechanism**: If the chatbot is asked to generate a hash, delegate to a utility function or API instead of the model.  

## Call to Action
To all AI chatbot developers: please be careful when implementing features involving hashing or other deterministic calculations. **Do not rely on AI for tasks that require mathematical precision** – always use standard libraries instead.  

---

✍️ _Reported by: [Riyan Hidayat Samosir - hanyajasa@gmail.com - hanyajasa.com]_  
📅 _Date: August 22, 2025 - Palangka Raya, Indonesia_  


_____


# ⚠️ Bug Report: Kesalahan Hashing (MD5) pada Banyak Chatbot AI

## Deskripsi Bug
Saya menemukan bug yang cukup sering terjadi pada berbagai Chatbot AI, khususnya saat diminta untuk menghasilkan **nilai hash (misalnya MD5)** dari sebuah string.  

Contoh kasus:  

**Input user:**  

Berapa MD5 dari: admin1


**Jawaban Chatbot (salah):**  

MD5 dari "admin1" adalah: 7c4a8d09ca3762af61e59520943dc264


Padahal nilai MD5 yang benar dari `admin1` adalah:  

e00cf25ad42683b3df678c61f42c6bda


## Dampak
- **Membingungkan pengguna**: User yang bergantung pada hasil hash akan mendapatkan informasi salah.  
- **Berbahaya untuk aplikasi nyata**: Hash biasanya dipakai dalam keamanan (password, verifikasi file, dsb). Kesalahan ini bisa menimbulkan kerentanan atau kesalahan sistem.  

## Penyebab
Kemungkinan besar chatbot tidak benar-benar menghitung hash, melainkan "menghafal" atau "mengira-ngira" jawaban dari pola teks sebelumnya.  

## Rekomendasi untuk Pengembang Chatbot
1. **Jangan lakukan hashing di model langsung** – gunakan fungsi hashing dari bahasa pemrograman (contoh: `hashlib` di Python).  
2. **Validasi hasil** dengan library resmi sebelum diberikan ke user.  
3. **Tambahkan fallback**: jika chatbot diminta menghasilkan hash, delegasikan ke fungsi utilitas eksternal, bukan hanya model.  

## Ajakan
Bagi semua pengembang chatbot AI: harap berhati-hati dalam mengimplementasikan fitur terkait hashing atau perhitungan deterministik lainnya. Sebaiknya **jangan mengandalkan AI untuk fungsi yang seharusnya presisi matematis**, melainkan panggil library resmi.  

---

✍️ _Ditemukan oleh: [Riyan Hidayat Samosir - hanyajasa@gmail.com - hanyajasa.com]_  
📅 _Tanggal: 22 Agustus 2025 - Palangka Raya, Indonesia_  
