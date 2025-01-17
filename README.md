# **EthioMart eCommerce**  

## **Overview**  
EthioMart Telegram Scraper is a Python-based tool designed to extract structured data from Ethiopian e-commerce Telegram channels. The scraper retrieves historical messages, monitors new messages in real time, and stores extracted data in a structured format, including text, metadata, and media. Additionally, EthioMart employs a fine-tuned LLM for Amharic Named Entity Recognition (NER) to extract key business entities such as product names, prices, and locations from the collected data.

## **Features**  
✅ **Historical Data Scraping** – Extracts up to 10,000 past messages per channel.  
✅ **Real-Time Monitoring** – Captures new messages instantly as they are posted.  
✅ **Media Handling** – Downloads and stores images from Telegram messages.  
✅ **Structured Data Storage** – Saves data in CSV and CoNLL formats for further processing.  
✅ **Amharic NER** – Fine-tuned LLM to extract product names, prices, and locations.  
✅ **Scalable & Customizable** – Easily add more channels for scraping.  

---

## **Installation**  

### **1. Clone the Repository**  
```bash
git clone https://github.com/Azazh/EthioHub.git
cd EthioHub
```

### **2. Install Dependencies**  
```bash
pip install -r requirements.txt
```

### **3. Set Up Environment Variables**  
Create a `.env` file in the project root and add your Telegram API credentials:  
```
TG_API_ID=your_api_id
TG_API_HASH=your_api_hash
phone=your_phone_number
```
🔹 **Get API credentials** from [my.telegram.org](https://my.telegram.org/apps).  

---

## **Usage**  

### **1. Start Historical Data Scraping**  
Extract messages from selected channels and store them in `telegram_data.csv`:  
```bash
python telegram_scraper.py
```

### **2. Enable Real-Time Monitoring**  
Automatically log new messages from specified channels:  
```bash
python real_time_monitor.py
```

### **3. Preprocess Extracted Data**  
Preprocess text data, tokenize, and normalize Amharic text:  
```bash
python preprocess_data.py
```

### **4. Label Data for NER (CoNLL Format)**  
A subset of the dataset is manually labeled in the CoNLL format to train the Amharic NER model. Example:
```
በልዩ ዋጋ B-PRICE
1000 I-PRICE
ብር I-PRICE
እንዲሁም O
በ B-LOC
አዲስ B-LOC
አበባ I-LOC
ይገኛል O
```
Labeled data is stored in `data/labeled_amharic_data.conll`.

---

## **Project Structure**  
```
.
├── .github
│   └── workflows
│       └── unittests.yml
├── .vscode
├── data
│   ├── labeled_amharic_data.conll
│   ├── preprocessed_telegram_data.csv
│   ├── telegram_data.csv
│   ├── telegram_data.xlsx
│   ├── tokens_labels.conll
├── notebooks
│   ├── data_ingestion_and_data_preprocessing.ipynb
│   ├── label_dataset_conll_format.ipynb
├── scripts
│   └── preprocess_data.py
├── src
├── tests
├── venv
├── .env
├── .gitignore
├── LICENSE
```

---

## **Data Format**  
Extracted data is saved in `telegram_data.csv` with the following fields:  
| Channel Title | Channel Username | Message ID | Message Text | Date | Media Path |
|--------------|-----------------|------------|--------------|------|------------|
| FashionTera | @fashiontera | 12345 | "New dresses available!" | 2024-01-01 | photos/fashiontera_12345.jpg |

Labeled data is stored in CoNLL format for NER model training.

---

## **Next Steps**  
🔹 Fine-tune and train the Amharic NER model on the labeled dataset.  
🔹 Implement automated entity recognition and structured data extraction.  
🔹 Optimize data retrieval and storage for large-scale monitoring.  

---

## **Contributing**  
Want to improve this project? Fork the repo and submit a pull request!  

---

## **License**  
📜 MIT License – Feel free to use and modify this project.  

---

🚀 **EthioMart Telegram Scraper** helps businesses extract and analyze e-commerce data efficiently!
