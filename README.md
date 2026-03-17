# ⌨️ Localboard

### The Ultimate Local LLM AI Keyboard for Android

<p align="center">
  <img src="https://img.shields.io/badge/platform-Android-green">
  <img src="https://img.shields.io/badge/engine-llama.cpp-orange">
  <img src="https://img.shields.io/badge/license-MIT-blue">
</p>

---

## 🎥 Demo (1m 32s)

Direct video link:
https://github.com/user-attachments/assets/ac5d0945-04e6-4a5f-b4f6-e5f37cfb68f4

---
  <video controls width="850">
    <source src="https://github.com/user-attachments/assets/ac5d0945-04e6-4a5f-b4f6-e5f37cfb68f4" type="video/mp4">
  </video>
## 🚀 What is Localboard?

**Localboard** is an open-source Android keyboard that runs **Large Language Models locally on your device**.

No cloud APIs.
No telemetry.
No remote inference.

Models like **Phi-3, TinyLlama, and SmolLM** run directly on your phone using `llama.cpp`.

Your AI assistant works **offline, instantly, and privately inside every Android app.**

---

## ✨ Features

### 🔒 Privacy First

* 100% offline inference
* No data leaves your phone
* No API keys required

### ⚡ High Performance

* ARM **dotprod + fp16 acceleration**
* **Flash Attention** support
* **Q8 KV Cache**
* 30+ tokens/sec on modern phones

### 🧠 AI Writing Assistant

* Rewrite messages professionally
* Fix grammar instantly
* Summarize text
* Chat with local models

### 🧩 Works Everywhere

Use Localboard in:

* WhatsApp
* Gmail
* Discord
* Twitter
* Any Android text field

---

## 🏗 Architecture

Localboard uses a **multi-process architecture** so inference never blocks the keyboard UI.

Keyboard UI (IME process)
│
│ AIDL IPC
▼
Inference Service (:inference process)
│
▼
llama.cpp runtime (JNI)
│
▼
GGUF model

---

## 🛠 Tech Stack

| Component     | Technology      |
| ------------- | --------------- |
| Language      | Kotlin + C++    |
| UI            | Jetpack Compose |
| Inference     | llama.cpp       |
| Native Bridge | JNI             |
| IPC           | AIDL            |
| Build         | CMake           |

---

## 📦 Supported Models

Localboard supports **any GGUF model**.

| Model          | Size   | Speed             |
| -------------- | ------ | ----------------- |
| SmolLM-135M    | ~90MB  | ⚡ 30+ t/s         |
| TinyLlama-1.1B | ~640MB | ⚡ 10-15 t/s       |
| Phi-3 Mini     | ~2.2GB | 🧠 Best reasoning |

---

## 📥 Installation

### Clone the repository

git clone https://github.com/datta256/gamerr.git
cd gamerr
git submodule update --init --recursive

### Build

Open in Android Studio and build the **Release variant**.

### Enable Keyboard

1. Open Localboard
2. Enable it in Android keyboard settings
3. Switch input method to **Localboard**

---

## 🔧 Performance Optimizations

Localboard uses several native optimizations:

* `use_mmap = true` for instant model loading
* `n_threads = 4` bound to performance cores
* Flash Attention
* KV cache quantization

These allow **real-time token streaming on mobile CPUs**.

---

## 🤝 Contributing

PRs welcome. Areas of interest:

* Emoji keyboard support
* Vulkan backend
* Model manager improvements
* UI improvements

---

## 📄 License

MIT License
