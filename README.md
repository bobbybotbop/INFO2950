# INFO2950

This INFO 2950 project analyzes sales and inventory data from a family business. It combines transaction records with product details to examine what the business sells and purchases, when these activities occur, and at what prices.

## Group Members

- William Chen
- May Wu
- Clement Roze
- Joshua Chen
  
## Datasets

1. **Sales transactions:** Individual sales, including the date, product, quantity, price, and payment method.
2. **Inventory purchases:** Supplier restocks, including the date, product, quantity, unit cost, and supplier.
3. **Product information:** Product details such as color, material, hat style, size, and listed price.

## Data Availability
Our primary dataset is a CSV file exported directly from the accounting software used by a family business. Since the data is provided as an existing export, we will not need to use an API or web scraping. The dataset contains historical transaction records dating back to the early 2000s.

Because the project uses a single private business dataset, there are no public online data sources or APIs to link to. The data will instead be analyzed directly from the provided CSV file.

## Data Trustworthiness
The data was collected through the accounting software used by the family business. The same software and data-recording process were used throughout the period covered by the dataset, which provides consistency across the records.

Why we trust the data:
- The data comes directly from the business's accounting system rather than being manually compiled for this project.
- The same collection process was used over many years.
- The dataset contains records dating back to the early 2000s, providing a substantial historical record.

## Limitations
- Product descriptions, particularly colors, are not always standardized. For example, similar straw colors may be recorded as "raffia," "natural," or "beige," and some entries may contain spelling variations.
- The data consists of transaction records rather than pre-processed popularity measures. Therefore, we will need to process and aggregate the transactions ourselves to determine measures such as item popularity or sales trends.

<img width="680" height="573" alt="image" src="https://github.com/user-attachments/assets/245ae870-eeec-4ed3-b00a-312714e04b01" />
