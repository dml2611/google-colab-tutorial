# Getting Started with Google Colab Notebook from Your Gmail Account

This tutorial will guide you through the steps to open a Google Colab notebook using your Gmail account.

## Step 1: Sign in to Your Gmail Account
1. Open your web browser.
2. Go to [Gmail](https://mail.google.com).
3. Enter your email address and password to sign in.

## Step 2: Access Google Colab
1. Once you are logged into your Gmail account, click on the Google Apps icon (a grid of nine dots) in the upper right corner of the Gmail interface.
2. Scroll down or search for "Colab" and click on it. Alternatively, you can directly go to [Google Colab](https://colab.research.google.com).

## Step 3: Create or Open a Notebook
1. On the Google Colab landing page, you will see options to create a new notebook or open an existing one.
2. To create a new notebook:
   - Click on `File` -> `New notebook`.
   - A new untitled notebook will open where you can start writing code immediately.
3. To open an existing notebook:
   - Click on `File`.
   - Select `Open notebook`. 
   - Choose the source of your notebook:
     - "Google Drive" to access notebooks stored in your Google Drive.
     - "GitHub" to access notebooks from a GitHub repository.
     - "Upload" to upload a notebook from your local computer.
     - "Recent" to open recently accessed notebooks.
4. Mounting Google Drive (Optional)
   - If your notebook needs access to files stored in your Google Drive:
   - Add the following code snippet to a code cell in your Colab notebook:

     ```python
     from google.colab import drive
     drive.mount('/content/gdrive')
     ```
   - Follow the link provided, select your Google account, and grant permissions.
   - After authorization, you will receive a code to paste into the notebook which will mount your Google Drive.

## Step 4: Using the Colab Notebook
1. Once the notebook is opened, you can start writing and running code in the cells.
2. Execute code cells by clicking on the play button or using `Shift` + `Enter`.
3. You can also rename the notebook by clicking on the title at the top.
4. Interact with the notebook interface to add text, code, and visualizations.

## Step 5: Saving Changes
1. Colab autosaves your notebook periodically.
2. You can manually save your changes by clicking on `File` -> `Save` or pressing `Ctrl` + `S` (`Cmd` + `S` on Mac). Alternatively, you can go to `File` -> `Save a copy in Drive`.
4. You can also save your file on GitHub by going to `File` -> `Save a copy in GitHub`. Choose your repository and branch, then click `OK` to save."

---

## Reading a CSV File from Google Drive

   Once Google Drive is mounted, you can read a CSV file using Pandas:

   ```python
   # Importing necessary libraries
   import pandas as pd

   # Mount Google Drive to access files
   from google.colab import drive
   drive.mount('/content/gdrive')

   # Path to the CSV file in your Google Drive
   file_path = '/content/drive/My Drive/path/to/your/file.csv'

   # Reading the CSV file into a Pandas DataFrame
   df = pd.read_csv(file_path)

   # Displaying the first few rows of the DataFrame
   print(df.head())
   ```
---

# Reading an Excel File from Google Drive

   Once Google Drive is mounted, you can read an Excel file using Pandas:
   ```python
   # Importing necessary libraries
   import pandas as pd

   # Mount Google Drive to access files
   from google.colab import drive
   drive.mount('/content/gdrive')

   # Path to the Excel file in your Google Drive
   file_path = '/content/drive/My Drive/path/to/your/file.xlsx'

   # Reading the Excel file into a Pandas DataFrame
   df = pd.read_excel(file_path)

   # Displaying the first few rows of the DataFrame
   print(df.head())
   ```
---

## Additional Resources
- **Google Colab Documentation:** Official documentation for Google Colab.
- **GitHub Repository:** Create a GitHub repository to store and share your Colab notebooks with others. 

By following these steps, you can easily access and start working on Google Colab notebooks from your Gmail account.
