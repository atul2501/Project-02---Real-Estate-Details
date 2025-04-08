## 🏙 Thane Real Estate Scraper - 99acres.com 🕵️‍♂️

This project is a Python-based **web scraper** that extracts **real estate listings from 99acres.com**, specifically for the **Thane** region. It uses **Selenium** to automate a headless browser and scrapes data such as title, price, location, configuration, and more. The final data is exported as a CSV file for further analysis.

---

### 🚀 Features

- Scrapes multiple pages of listings automatically from 99acres
- Gathers key property details like price, size, location, and features
- Stores clean data in `df_properties.csv`
- Uses stealth Chrome options to bypass bot detection
- Handles missing data and waits for page elements properly

---

### 📦 Output Sample

The script saves the data in a CSV file named:

```
df_properties.csv
```

Sample columns:
- Property Title
- Price
- Location
- Beds/Baths
- Area
- Furnishing
- Transaction Type
- Property Type

---

### 🛠️ Requirements

Install dependencies via pip:

```bash
pip install -r requirements.txt
```

**requirements.txt**
```
selenium
pandas
```

Also make sure to download and install the [ChromeDriver](https://sites.google.com/chromium.org/driver/) version matching your Chrome browser, and add it to your system PATH.

---

### 📑 How to Run

1. Clone this repo
2. Install the requirements
3. Open and run `restructured_99acer.ipynb` using Jupyter Notebook  
   OR  
   Convert it to a Python script and run from terminal

```bash
jupyter notebook restructured_99acer.ipynb
```

---

### ⚙️ ChromeDriver Options

This script uses special Chrome options to reduce bot detection:

```python
chrome_options.add_argument("--incognito")
chrome_options.add_argument("--disable-blink-features=AutomationControlled")
chrome_options.add_argument("--ignore-certificate-errors")
chrome_options.add_argument("--enable-features=NetworkServiceInProcess")
chrome_options.add_argument("--disable-features=NetworkService")
```

---

### 📈 Future Plans

- Add custom filters (price range, BHK, area, etc.)
- Export to Excel or JSON
- Add GUI to browse results visually

---

### 👨‍💻 Author

Made with ❤️ by [@atul2501](https://github.com/atul2501)
