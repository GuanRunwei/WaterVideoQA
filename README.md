# 🌊 WaterVideoQA: A Benchmark for ASV-Centric Perception and Rule-Compliant Reasoning

<p align="center">
  <a href="[https://arxiv.org/abs/xxxx.xxxx](https://arxiv.org/abs/xxxx.xxxx)"><img src="[https://img.shields.io/badge/Paper-arXiv-red](https://img.shields.io/badge/Paper-arXiv-red)"></a>
  <a href="[https://pan.baidu.com/s/xxxx](https://pan.baidu.com/s/xxxx)"><img src="[https://img.shields.io/badge/Dataset-Baidu_Netdisk-blue](https://img.shields.io/badge/Dataset-Baidu_Netdisk-blue)"></a>
  <a href="[https://github.com/your-username/WaterVideoQA](https://github.com/your-username/WaterVideoQA)"><img src="[https://img.shields.io/github/stars/your-username/WaterVideoQA](https://img.shields.io/github/stars/your-username/WaterVideoQA)"></a>
</p>

<p align="center">
  <strong>The first large-scale, comprehensive Video Question Answering benchmark specifically engineered for all-waterway environments.</strong>
</p>

---

## 📢 News
* **[2026.05]** 🌊 The `WaterVideoQA` dataset (videos + annotations) is officially released via Baidu Netdisk!
* **[Coming Soon]** 🚀 The inference code for our multi-agent reasoning framework, **NaviMind**, is under clean-up and will be released soon. Stay tuned!

---

## 📊 About WaterVideoQA Dataset

While autonomous navigation has achieved remarkable success in passive perception, bridging the gap toward complex cognitive reasoning is critical for Autonomous Surface Vessels (ASVs). To this end, we introduce **WaterVideoQA**.

### 🌟 Dataset Highlights
- **Large Scale**: Contains **3,029 video clips** and **3,673 QA pairs** tailored for maritime navigation[cite: 5].
- **High Diversity**: Covers **6 distinct waterway categories** (River, Lake, Canal, Moat, Harbor, and Sea) featuring volatile lighting and dynamic weather[cite: 5].
- **Cognitive Hierarchy**: Stress-tests models across a rigorous **5-tier cognitive framework**[cite: 5]:
  1. `Perception` (Object recognition & attributes)
  2. `Scene Understanding` (Environmental context)
  3. `Action / Interaction` (Dynamic vessel behaviors)
  4. `Causal & Predictive` (Collision risk & trajectory prediction)
  5. `Knowledge-Driven` (Rule-compliant reasoning based on COLREGS)

---

## 📥 Dataset Download

The complete dataset (including raw video files and JSONL annotations) is currently hosted on Baidu Netdisk (百度网盘). 

* 🔗 **Baidu Netdisk Link**: [Click here to download](https://pan.baidu.com/s/1gvMHblspmNxKukiadq6q4g)
* 🔑 **Extraction Code (提取码)**: `casv`

*Note: The dataset contains high-resolution video clips. Please ensure you have sufficient storage space before downloading.*

---

## 📂 Data Structure

The annotations are provided in `JSONL` format. Each line represents a unique QA sample associated with a specific video clip.

### Example Format
```json
{
  "id": 0, 
  "video": "lars_yt026_07.mp4", 
  "category": "Action/Interaction QA", 
  "conversations": [
    {"from": "human", "value": "<video>\nIs the current red vessel in the right front side docking?"}, 
    {"from": "gpt", "value": "Yes, the vessel appears to be docked. It is stationary and positioned near the shore, with no visible signs of movement or towing."}
  ], 
  "duration": 2.0
}
