<div align="center">

# 🎙️ Voice-to-3D

### Say it. See it. Grab it.
**Generative AI for real-time generation of 3D objects in Augmented Reality**

<!-- ![Demo](docs/demo.gif) -->

</div>

---

## ✨ What is this?

AR is powerful, but it's only as rich as the 3D assets it can show, and those are normally modelled by hand and bundled in advance.

**Voice-to-3D removes that bottleneck.** Put on the headset, say *"a wooden chair"*, and within about **three seconds** a textured 3D hologram appears in front of you. Grab it, move it, rotate it, scale it, all with bare hands.

> 🗣️ **Speak** → 📝 **Transcribe** → 🖼️ **Imagine** → 🧊 **Reconstruct** → 🕶️ **Hold it in your hands**

---

## 🧠 How it works

```
┌──────────────────┐      audio       ┌─────────────────────────────────────┐
│  Magic Leap 2    │ ───────────────► │        Dockerized GPU server        │
│                  │                  │                                     │
│  • Hand menu     │                  │  1. ASR            (speech → text)  │
│  • Voice capture │                  │  2. Text-to-image  (text → image)   │
│  • Hologram view │ ◄─────────────── │  3. Image-to-3D    (image → mesh)   │
│  • Hand gestures │   GLB + text     │                                     │
└──────────────────┘                  └─────────────────────────────────────┘
```

1. **Open the hand-anchored menu** and describe an object by voice.
2. The audio is sent to a **remote GPU server** (these models are too heavy for standalone AR hardware).
3. The server runs **ASR → text-to-image → image-to-3D** and returns a **textured GLB mesh**.
4. The transcription shows up as soon as the audio is sent, and the hologram follows right after.
5. Interact with it using **bare-hand gestures**: grab, move, rotate, scale.

---

## 🚀 Highlights

| | |
|---|---|
| ⚡ **Real-time** | ~3 s end-to-end latency, fast enough for a continuous speak-and-see flow |
| 🧪 **Evidence-based** | Every model in the chain was picked through dedicated evaluation, not assumption |
| 🏎️ **Optimized export** | Export optimization cuts TRELLIS generation from **~44 s to ~10 s** |
| 🖐️ **Hands-on** | Grab, move, rotate and scale holograms with bare hands |
| ✅ **Validated usability** | **SUS 82.64** (n = 18) on the final AR application |
| 🐳 **Easy to deploy** | Backend runs as a Docker container on a GPU machine |

---

## 📊 Evaluation

- **Image-to-3D benchmark:** four models compared on the quality–speed trade-off, with a speed-constrained criterion for choosing among them.
- **Text-to-image preference study:** blind study with **n = 35** participants validating the image-generation stage.
- **Usability study:** System Usability Scale with **n = 18**, scoring **82.64**, plus application-specific feedback.

### How it compares

| System | Input | Latency | Study |
|---|---|---|---|
| Dream Mesh | Speech | ~30–40 min | None |
| Transc. Dim. | Image | ~68 s | SUS 69.6 |
| Matrix | Speech | < 50 s | SUS 69.6 |
| Say It See It | Speech | 18–74 s | Likert |
| **Voice-to-3D (ours)** | **Speech** | **~3 s** | **SUS 82.6** |


---

## 📬 Contact

- Rafael Conceição: rafaelpc02@gmail.com

---

<div align="center">

**If you like this project, give it a ⭐**

</div>
