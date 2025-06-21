# ReflectiveInjection

This project explains the concepts of **Reflective Injection** technique, including analysis and development of a reflective loader.

---

## 🎯 Mục tiêu

- ✨ Viết một Reflective Loader
- 🧠 Tải payload dạng **DLL hoặc shellcode**, **KHÔNG ghi file**
- 🧰 **Manual Map** toàn bộ DLL như Windows loader thực hiện
- 🔍 Crawl **PEB** để resolve API
- 🚀 Jump trực tiếp vào EntryPoint (`DllMain` / `DllEntry`)

---

## 📁 Cấu trúc thư mục

```text
ReflectiveLoader/
├── main.cpp           # Loader chính (có thể shellcode hóa)
├── reflective_dll.c   # Logic mapping DLL từ memory
├── reflective_dll.h   # Header của reflective DLL
├── payload.dll        # DLL payload (phải export DllMain)
├── build_payload.bat  # Build DLL thành shellcode (vd: dùng sRDI)
├── utils_pe.h         # Helpers: GetNTHeaders, RVA2VA, v.v.
└── Makefile / build.ps1
