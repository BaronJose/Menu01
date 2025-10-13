# How to Use the Google Sheet for the Digital Menu

This document explains how to add, edit, and structure items in your Google Sheet to correctly display them on the digital menu. The menu is designed to update automatically when you change the sheet.

---
## Quick Setup

Before you begin, make sure your Google Sheet is published correctly.

1.  Go to **File** -> **Share** -> **Publish to web**.
2.  Under the **Link** tab, ensure your menu sheet is selected.
3.  In the second dropdown, select **Comma-separated values (.csv)**.
4.  Click **Publish** and copy the generated URL. This is the link that goes into the code.

---
## Understanding the Columns

Your sheet **must** have these exact column headers in the first row. The order is important.

| Header      | Purpose                                                                                              |
| :---------- | :--------------------------------------------------------------------------------------------------- |
| `Category`  | Groups items together. Items with the same category name will appear in the same column on the menu. |
| `ItemName`  | The name of the dish or item.                                                                        |
| `Price`     | The price of the item. Include the `$` sign.                                                         |
| `Description`| A short, italicized description that appears below the item name.                                    |
| `ImageURL`  | **Only used for the footer.** A direct link to an image file (e.g., ending in `.jpg` or `.png`).      |

---
## Formatting Your Menu Items

You can control the layout by how you enter data in the rows.

### 1. Standard Menu Item

This is the most common entry. Fill in the `ItemName` and `Price`. The `Description` is optional.

| Category  | ItemName | Price  | Description            |
| :-------- | :------- | :----- | :--------------------- |
| Antojitos | Nachos   | $6.50  | Con queso y jalapeños  |

### 2. Sub-heading

To create a bold sub-heading within a category (like "AGUAS FRESCAS"), type the heading in the **`ItemName`** column **IN ALL CAPS** and leave the **`Price`** column empty.

| Category | ItemName       | Price |
| :------- | :------------- | :---- |
| Bebidas  | **AGUAS FRESCAS** |       |

### 3. Price Line

To create a centered price line for a group of items (like for juices), leave the **`ItemName`** column empty and type the price text into the **`Price`** column.

| Category | ItemName | Price                     |
| :------- | :------- | :------------------------ |
| Jugos    |          | **Mediano $10 \| Grande $14** |

### 4. Splitting Long Categories

If a category has too many items to fit vertically, simply split the list by creating a new category name. The code will automatically place it in a new column.

-   **Example:**
    -   `Antojitos` (for the first 7 items)
    -   `Más Antojitos` (for the next 7 items)

---
## Adding Footer Images

To add a picture to the rotating footer carousel:

1.  Set the **`Category`** to **`Footer`**. This is case-sensitive.
2.  Add the **`ItemName`** and **`Price`** for the text that will appear below the image.
3.  Paste the direct image link into the **`ImageURL`** column.

| Category | ItemName | Price  | ImageURL                                      |
| :------- | :------- | :----- | :-------------------------------------------- |
| **Footer** | Churros  | $5.00  | `https://your-site.com/images/churros.jpg`    |