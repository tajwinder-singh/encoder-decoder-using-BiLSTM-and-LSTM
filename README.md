# 𝐁𝐮𝐢𝐥𝐝𝐢𝐧𝐠 𝐄𝐧𝐜𝐨𝐝𝐞𝐫–𝐃𝐞𝐜𝐨𝐝𝐞𝐫 𝐌𝐨𝐝𝐞𝐥𝐬 𝐰𝐢𝐭𝐡 𝐋𝐒𝐓𝐌 & 𝐁𝐢𝐋𝐒𝐓𝐌 𝐟𝐨𝐫 𝐒𝐞𝐪𝐮𝐞𝐧𝐜𝐞-𝐭𝐨-𝐒𝐞𝐪𝐮𝐞𝐧𝐜𝐞 𝐋𝐞𝐚𝐫𝐧𝐢𝐧𝐠

From past four days, I have been implementing an Encoder–Decoder architecture from scratch — using **BiLSTM and LSTM** — to understand how modern translation models process sequences.  
I already knew how to implement the **RNNs (LSTM, GRU, BiLSTM)**.

---

## •  Steps I Followed

### **1. Data Preprocessing**
- Lowercased all sentences for uniformity.  
- Used `nlp.pipe` for efficient sentence batching.  
- Saved English–French datasets as `.json` with proper UTF-8 encoding (`ensure_ascii=False`).

---

### **2. Symbol & Length Analysis**
- Checked non-alphabetic symbols across the corpus.  
- Computed maximum sentence length using the **90th percentile** — a balance between memory and coverage.

---

### **3. Subword Tokenization**
- Instead of traditional tokenization (which causes OOM issues with large vocabularies), used **SentencePiece** for subword-level tokenization.  
- Example: *“Playful” → “Play” + “ful”*  
- This significantly reduced vocabulary size and memory footprint during training.

---

### **4. Building the Model**
- Designed an **Encoder–Decoder (Seq2Seq)** model using **LSTM/BiLSTM** layers.  
- Added **attention-ready architecture** for future expansion.  
- Trained the model on preprocessed English–French pairs.

---

### **5. Inference Phase**
- Built a separate **inference model** to generate translations token-by-token.  
- The encoder provides hidden states, which the decoder uses iteratively to predict the next token.

---

## • Learnings

1. **Subword tokenization** prevents memory overflow and improves vocabulary efficiency.  
2. **LSTM and BiLSTM** capture contextual dependencies effectively in both directions.  
3. Designing **separate inference pipelines** is crucial for real-world translation tasks.  
4. **90th percentile max-length selection** keeps training efficient without major data loss.

---

🔗 **LinkedIn:** [https://linkedin.com/tajwinder-singh-](https://www.linkedin.com/in/tajwinder-singh-)
---

#DeepLearning #NLP #Seq2Seq #LSTM #BiLSTM #EncoderDecoder #MachineLearning #LanguageTranslation #AI #DataScience #NeuralNetworks
<img width="1365" height="629" alt="image" src="https://github.com/user-attachments/assets/b7845ac9-5a4f-4391-ba92-a3884445ac97" />
