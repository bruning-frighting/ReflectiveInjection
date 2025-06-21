# ReflectiveInjection
Explain the concepts of Reflective Injection technique as well as its analysis and development
Mục tiêu:
Viết Reflective Loader

Tải payload dạng DLL hoặc shellcode, KHÔNG GHI FILE

Manual Map toàn bộ DLL như Windows loader

Crawl PEB để resolve API

Jump vào EntryPoint (DllMain/DllEntry)

ReflectiveLoader/
├── main.cpp          # Loader chính (có thể shellcode hóa)
├── reflective_dll.c  # Logic mapping DLL từ memory
├── reflective_dll.h
├── payload.dll       # DLL payload (exported DllMain)
├── build_payload.bat # Build DLL thành shellcode
├── utils_pe.h        # Helpers: GetNTHeaders, RVA2VA, etc
└── Makefile / build.ps1
