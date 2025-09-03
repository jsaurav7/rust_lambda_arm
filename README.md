# Rust Lambda ARM Template

A starter template to build and package **Rust AWS Lambda functions** targeting **ARM (Graviton2)** on the **Amazon Linux runtime** using **musl static linking**.  

This repo is set up with:
- ✅ **GitHub Actions** to automatically build your Lambda binary for `aarch64-unknown-linux-musl`.
- ✅ **Static musl binaries** — no dynamic dependencies, fully self-contained.
- ✅ **Stripped binaries** for minimal size (faster cold starts, reduced package size).
- ✅ **Deployment-ready artifact** — outputs a `.zip` bundle you can upload directly to AWS Lambda (ARM64 runtime).
- ✅ **Simple project structure** you can extend with your own code.

---

## 📦 How it Works
1. On push/merge, GitHub Actions:
   - Cross-compiles your Rust code for **ARM64 (musl)**.
   - Strips symbols to reduce binary size.
   - Packages the binary into a `.zip` file.
2. The final `.zip` is available as a **GitHub Actions artifact**, ready to upload to Lambda.

---
