
# **Data-Mining Project**

## **Project Overview**
In this project, we act as consultants for **ABCDE Eats Inc. (ABCDE)**, a fictional food delivery service partnering with a range of restaurants to offer diverse meal options. Our task is to analyze customer data collected over three months from three cities to help ABCDE develop a **data-driven strategy** tailored to various customer segments. The description of the data is provided under the **Dataset Description** section of this document.  

We segment customers using multiple perspectives. Examples of segmentation perspectives include:  
- **Value-based segmentation** – Groups customers by their economic value.  
- **Preference or behavior-based segmentation** – Focuses on purchasing habits.  
- **Demographic segmentation** – Categorizes customers by attributes like age, gender, and income to understand different interaction patterns.  

Ultimately, the goal is to develop a **final segmentation** that integrates these perspectives, enabling ABCDE to craft a **comprehensive marketing strategy**.  

---

## **Interactive Application Development**  

To complement our analysis, we developed an **interactive application** that allows users to explore and visualize the customer segmentation results dynamically. The development was carried out using a **robust and user-friendly technology stack**, selected for its compatibility with **Python** and its efficiency in handling **data analysis and visualization** tasks.  

### **Technologies Used**
- 🐍 **Python** – Core programming language for data processing and application development.  
- 🎨 **Streamlit** – Used to build the **interactive interface** for real-time data exploration.  
- 📊 **Pandas** – For **data manipulation and preprocessing**.  
- 📈 **Plotly** – Used to generate **interactive visualizations**, including a **3D scatter plot** for cluster analysis.  
- 🔄 **Pickle** – Used to **import the scaler and the preprocessed data**, ensuring consistency in transformations applied during model training and deployment.  

This application enhances the accessibility of our segmentation insights, allowing stakeholders to interactively explore customer clusters and gain a deeper understanding of their characteristics.  

---

## **Notes & Considerations**  

### **Missing Data Imputation**  
- We should have **imputed numerical variables using a central tendency measure** (such as mean, median, or mode) or applied **KNN imputation** instead of solely using the mode.  
- **Imputing with the mode assumes a normal distribution**, which can distort the data’s original distribution, **introducing bias and reducing variance**.  
- However, in this case, we assumed normality, where **mode and median coincide**, minimizing this effect.  

### **Outlier Treatment**  
- Our goal was to retain **"unusual but meaningful groups"** (e.g., extreme but coherent clusters), which **DBSCAN** effectively handles by distinguishing **true noise from dense clusters**.  
- **Winsorization**, on the other hand, would **indiscriminately cap values**, potentially altering these meaningful extreme groups.  
- **Boxplot analysis** revealed that:  
  - **Median values remained unchanged**.  
  - **Spread (index rates) before and after outlier removal was similar**, indicating **outliers were sparse and their removal had minimal impact on central tendencies**.  
  - This aligns with **DBSCAN’s strength** in identifying **true noise while preserving meaningful extreme points**.  
- **Winsorization should only be used when removing rows is unacceptable**, as it alters the distribution rather than filtering noise selectively.  

---

## **Final Thoughts**  
By integrating **customer segmentation analysis** with an **interactive visualization tool**, we provide ABCDE with a **data-driven strategy** that is both **insightful and actionable**. The combination of **advanced clustering techniques** and a **user-friendly interface** ensures that ABCDE can **effectively target different customer segments**, optimize marketing efforts, and improve overall business performance.  

