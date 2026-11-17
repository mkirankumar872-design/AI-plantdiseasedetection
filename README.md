# AgroVision: Plant Disease Detector & Treatment Advisor
> An AI-powered Computer Vision & Agricultural Diagnostic Web Application for farmers, researchers, and agriculture students.

---

## 🌟 PRD Feature Implementation Breakdown

| Feature ID | PRD Requirement | Implementation in AgroVision |
| :--- | :--- | :--- |
| **FEAT-01** | **Image Upload & Live Camera Capture** | • Drag-and-Drop file uploader (JPEG/PNG/WEBP up to 10MB)<br>• Web/Mobile live camera integration with device camera flip<br>• 4 Pre-loaded high-resolution sample leaf cards for 1-click test runs |
| **FEAT-02** | **Image Preprocessing** | • Automatic client-side and server-side dimension rescaling to 224x224<br>• RGB normalization & HSV color channel map extraction<br>• Necrotic lesion segmentation and pixel density scanning |
| **FEAT-03** | **AI Disease Classification** | • Dual engine: Offline PlantVillage Neural Classifier + Cloud Google Gemini Multimodal Vision API<br>• Outputs exact disease label, pathogen species, crop identification, and confidence percentage (e.g. 96.8%) |
| **FEAT-04** | **Remedy & Treatment Engine** | • **Organic Remedies**: Neem oil formulations, biocontrols (*Bacillus subtilis*, *Trichoderma*), copper soaps<br>• **Chemical Treatments**: Contact & systemic fungicides, dosage per liter, Pre-Harvest Interval (PHI)<br>• **Urgent Action Protocol**: 3-step immediate field isolation checklist<br>• **Preventative Advice**: Crop rotation, airflow spacing, soil mulching |
| **FEAT-05** | **Prediction History Log** | • Persistent `localStorage` history table tracking past scans, diagnosis, and severity<br>• Printable Diagnostic Certificate (PDF ready with custom print stylesheet)<br>• 1-Click JSON export for agricultural field records |
| **Bonus** | **Multilingual & Audio Voice** | • English, Hindi (हिन्दी), and Spanish (Español) instant translation<br>• Web Speech API integration to read diagnosis and remedies aloud for field accessibility |

---

## 🚀 How to Run the Website

### Method 1: Instant Browser Launch (Zero Installation Required)
You can open the website immediately in any web browser without installing any tools:
1. Navigate to:
   ```
   C:\Users\mkira\.gemini\antigravity\scratch\agrovision\index.html
   ```
2. Double-click **`index.html`** or right-click -> **Open with Google Chrome / Edge / Firefox**.
3. All UI components, sample leaves, camera access, offline neural classifier, and treatment advisors work straight out of the box!

---

### Method 2: Run with Python Flask Backend
If you want to run the full client-server stack with API endpoints:
1. Open PowerShell or Terminal in this directory:
   ```bash
   cd C:\Users\mkira\.gemini\antigravity\scratch\agrovision
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. (Optional) Set your Google Gemini API key:
   ```bash
   $env:GEMINI_API_KEY="AIzaSyYourKeyHere"
   ```
4. Start the server:
   ```bash
   python app.py
   ```
5. Open your browser at:
   ```
   http://127.0.0.1:5000
   ```

---

## 🔬 Supported Crop & Disease Classes (PlantVillage Benchmark)
- **Tomato**: Early Blight (*Alternaria solani*), Late Blight, Leaf Mold, Bacterial Spot, Healthy
- **Potato**: Late Blight (*Phytophthora infestans*), Early Blight
- **Corn (Maize)**: Common Rust (*Puccinia sorghi*), Northern Leaf Blight
- **Bell Pepper**: Bacterial Spot, Healthy Foliage
- **Apple & Grape**: Scab, Black Rot, Esca (Black Measles)
