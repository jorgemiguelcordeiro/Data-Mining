# Data-Mining
In this project, we act as consultants for ABCDE Eats Inc. (ABCDE), a fictional food delivery service partnering with a range of restaurants to offer diverse meal options. Our task is to analyze customer data collected over three months from three cities to help ABCDE develop a data-driven strategy tailored to various customer segments. The description of the data is provided under the Dataset Description section of this document.

We segment customers using multiple perspectives. Examples of segmentation perspectives include value-based segmentation, which groups customers by their economic value; preference or behavior-based segmentation, which focuses on purchasing habits; and demographic segmentation, which categorizes customers by attributes like age, gender, and income to understand different interaction patterns.

Ultimately, the goal is to develop a final segmentation that integrates these perspectives, enabling ABCDE to craft a comprehensive marketing strategy.

Notes:
 - We should have imputed numerical variables using a central tendency measure (such as mean, median, or mode) or applied KNN imputation instead of solely using the mode. Imputing with the mode assumes a normal distribution, but this can distort the data’s original distribution, introducing bias and reducing variance. However, in this case, we assumed normality, where mode and median coincide, minimizing this effect.

 - In the outlier treatment, our goal was to retain "unusual but meaningful groups" (e.g., extreme but coherent clusters), which DBSCAN effectively handles by distinguishing true noise from dense clusters. Winsorization, on the other hand, would indiscriminately cap values, potentially altering these meaningful extreme groups.

 - Boxplot analysis revealed that median values remained unchanged and the spread (index rates) before and after outlier removal was similar, indicating that outliers were sparse and their removal had minimal impact 
   on central tendencies.
   This aligns with DBSCAN’s strength in identifying true noise while preserving meaningful extreme points.
   Winsorization should only be used when removing rows is unacceptable, as it alters the distribution rather than filtering noise selectively.
