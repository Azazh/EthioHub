# **EthioMart ecommerce**  

## **Overview**  
EthioMart Telegram Scraper is a Python-based tool designed to extract structured data from Ethiopian e-commerce Telegram channels. The scraper retrieves historical messages, monitors new messages in real time, and stores extracted data in a structured format, including text, metadata, and media.  

## **Features**  
✅ **Historical Data Scraping** – Extracts up to 10,000 past messages per channel.  
✅ **Real-Time Monitoring** – Captures new messages instantly as they are posted.  
✅ **Media Handling** – Downloads and stores images from Telegram messages.  
✅ **Structured Data Storage** – Saves data in a CSV file for further processing.  
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

---

## **Project Structure**  
```
.
├── .github
│ └── workflows
│ └── unittests.yml
├── .vscode
├── data
│ ├── labeled_amharic_data.conll
│ ├── labeled_data_conll.conll
│ ├── labeled_data.conll
│ ├── labeled_ner_data.conll
│ ├── merged_amharic_ner_data.conll
│ ├── preprocessed_telegram_data.csv
│ ├── qnashcom_labeled_data.conll
│ ├── telegram_data.csv
│ ├── telegram_data.xlsx
│ └── tokens_labels.conll
├── notebooks
│ ├── init.py
│ ├── data_ingestion_and_data_preprocessing.ipynb
│ └── label_dataset_conll_format.ipynb
├── scripts
│ └── init.py
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

---

## **Next Steps**  
🔹 Implement NLP-based entity recognition for price, location, and product detection.  
🔹 Train an AI model to categorize and analyze e-commerce trends.  
🔹 Optimize data retrieval for large-scale monitoring.  

---

## **Contributing**  
Want to improve this project? Fork the repo and submit a pull request!  

---

## **License**  
📜 MIT License – Feel free to use and modify this project.  

---

🚀 **EthioMart Telegram Scraper** helps businesses extract and analyze e-commerce data efficiently!
