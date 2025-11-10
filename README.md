
##  Vibe Match Assignment overview

The goal of this project is to develop a **semantic fashion recommendation engine** that understands user “vibes” and recommends the most relevant fashion products.  

The system takes a **vibe query** (e.g., *“boho chic”*, *“vintage royal glam”*, or *“sporty street style”*) and uses **text embeddings** combined with **cosine similarity** to recommend the **Top 3 fashion items** from a dataset of product descriptions.

This project demonstrates how **AI can capture human aesthetics and context** using Natural Language Processing (NLP) techniques — bridging creativity and data intelligence.

---

##  Embedding Model Used
> **Model:** `sentence-transformers/all-mpnet-base-v2` (Hugging Face)

The Hugging Face model was used instead of OpenAI’s `text-embedding-ada-002` because my **OpenAI free credits had expired**.  
This model offers **high-quality semantic embeddings** for free, making it ideal for experimentation in Google Colab without API costs.  
It effectively captures contextual meaning in text, enabling precise **vibe-to-product matching**.

---

##  Project Workflow

### **Step 1: Data Preparation**
- Created a dataset of **15 fashion products** containing:
  - `name` (product name)  
  - `desc` (short description)  
  - `vibes` (style or mood tags)
- Cleaned and structured the data for embedding generation.

### **Step 2: Embedding Generation**
- Used the `all-mpnet-base-v2` model to generate embeddings for each product description and vibe tags.
- Generated query embeddings (e.g., “vintage royal glam”) for comparison.
- Stored all embeddings as vectors for cosine similarity computation.

### **Step 3: Vector Search Similarity**
- Computed **cosine similarity** between user query embeddings and product embeddings.
- Ranked items by similarity score and displayed **Top 3 recommendations**.
- Implemented **edge handling**:
  - If no product exceeded the similarity threshold (0.3), the system displayed a fallback prompt.

### **Step 4: Test & Evaluation**
- Tested 3 vibe queries: “boho chic”, “elegant royal evening look”, “urban sporty street vibe”.
- Logged metrics such as **similarity score**, **performance label**, and **latency**.
- Plotted visualizations showing:
  - Similarity scores per query
  - Latency comparison

**Evaluation Snapshot:**

| Query | Top Product | Similarity | Performance | Latency (s) |
|--------|--------------|-------------|--------------|-------------|
| Boho chic festival outfit | Boho Maxi Dress | 0.781 |  Good | 0.42 |
| Elegant royal evening look | Silk Evening Gown | 0.734 |  Good | 0.45 |
| Urban sporty street vibe | Urban Street Hoodie | 0.615 |  Average | 0.39 |

**Average Latency:** 0.42 sec  
**Good Match Ratio:** 2 / 3 (≈ 67%)

### **Step 5: Reflection**
A reflection phase was completed to identify improvements, challenges, and future directions.

---

##  Improvements & Next Steps
-  Integrate **Pinecone or FAISS** for scalable, fast vector similarity search.  
-  Build a **Streamlit-based interface** for real-time vibe queries.  
-  Extend dataset with **color, fabric, and occasion features** to enhance diversity.  
-  Add **image + text multimodal embeddings (CLIP)** for richer context.  
-  Implement a **feedback-based learning loop** for personalized recommendations.

---

##  Edge Cases Handled
-  **No strong match:**  
  When similarity < 0.3, the system shows a friendly fallback message instead of irrelevant results.  
-  **Unseen queries:**  
  Tested with terms like “punk futuristic metallic” — returned the leather jacket or fallback prompt correctly.  
-  **Query re-encoding:**  
  Each user query is re-embedded dynamically to ensure fresh, accurate results.  
-  **Low-latency performance:**  
  All results generated within 0.5 seconds consistently.  
-  **Threshold tuning:**  
  Optimized between 0.25–0.4 for balanced precision and recall.

---

##  Key Learnings
- Gained hands-on experience in **semantic similarity, embeddings, and cosine search**.  
- Understood how **AI can interpret human aesthetics** and convert them into meaningful recommendations.  
- Learned the impact of **data richness** on model accuracy and vibe understanding.  
- Improved technical and analytical skills in **vector databases, NLP, and explainable AI**.  
- Built confidence in **AI system design, testing, and evaluation workflows**.

---

##  Why AI at Nexora

Artificial Intelligence at **Nexora** blends creativity, innovation, and data intelligence — perfectly aligning with my career goals.  
Through this project, I strengthened my ability to build **intelligent, user-centric systems** that understand human emotions and context, supporting Nexora’s vision of delivering **personalized, AI-driven experiences**.  

Working on this semantic recommendation engine enhanced my expertise in **machine learning, vector search, and explainable AI**, while refining my problem-solving and analytical skills.  
These capabilities will help me grow with Nexora in creating **innovative, data-informed solutions** that merge technical precision with human insight.

---

##  Deliverables
-  **Colab Notebook:** `Fashion_Vibe_Recommendation.ipynb`  
-  **Reflection Report:** `PavanKalyan_FashionVibeAI_ReflectionReport.pdf`  
-  **README Documentation (GitHub)**  
-  **Evaluation Graphs and Outputs**


---

##  Summary
This project demonstrates how **AI and NLP** can transform fashion recommendations by understanding human “vibes.”  
Using free, open-source tools and semantic models, I successfully created an efficient and intelligent recommendation system.  
It highlights my ability to apply **AI creatively and practically** — delivering personalized, explainable results that align with modern digital experiences.

---

👨‍💻 **Author:** *Pavan Kalyan Neelam*  
📅 **Submission:** AI Internship Assignment — Nexora  
📧 **Contact:** pavankalyan.neelam@example.com  
🌐 **GitHub:** [pavankalyan-ai](https://github.com/pavankalyan-ai)
