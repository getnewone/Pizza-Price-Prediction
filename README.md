# Sales Prediction Project

This project implements a machine learning model to predict daily sales and store status (Quiet/Normal/Busy) based on historical sales data.

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.9 or higher
- Jupyter Notebook
- pip (Python package installer)

## 🛠️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Sales-Prediction
   ```

2. **Create and activate a virtual environment (recommended)**
   ```bash
   # On Windows
   python -m venv venv
   .\venv\Scripts\activate

   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install required dependencies**
   ```bash
   pip install numpy pandas scikit-learn matplotlib jupyter openpyxl
   ```

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open the notebook**
   - Navigate to `Sale_prediction.ipynb` in the Jupyter interface
   - Click to open the notebook

## 📦 Required Dependencies

The project relies on the following Python packages:
- numpy (2.0.2 or higher)
- pandas (2.2.3 or higher)
- scikit-learn (1.6.1 or higher)
- matplotlib (3.9.4 or higher)
- openpyxl (for Excel file support)

## 📊 Dataset

The project expects a `sales.xlsx` file in the root directory with the following columns:
- order_date: Date of sale
- total_sale: Daily sales amount
- Status: Store status (Quiet/Normal/Busy)

Make sure to place your sales data file in the correct location before running the notebook.

## 🚀 Running the Project

1. Ensure all cells in the notebook are executed in order
2. The final cell contains a prediction function that can be used as follows:
   ```python
   new_date = '29-07-2015'
   predicted_sales, status = predict_sale_and_status(new_date)
   print(f"Total sales on [{new_date}] can be: {predicted_sales:.2f}")
   print(f"Status of the shop can be: {status}")
   ```

## 📝 Project Structure

```
Sales-Prediction/
│
├── Sale_prediction.ipynb    # Main Jupyter notebook
├── sales.xlsx              # Dataset file
└── README.md               # Project documentation
```

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements.

## ❗ Troubleshooting

1. If you encounter a "Module not found" error:
   - Ensure all required packages are installed using pip
   - Verify your virtual environment is activated

2. If you see date parsing warnings:
   - This is expected behavior and doesn't affect the functionality
   - You can specify dayfirst=True in pd.to_datetime() to suppress the warning

3. For Excel file related errors:
   - Verify that openpyxl is installed
   - Check if the sales.xlsx file is present in the correct location
   - Ensure the file is not corrupted or open in another program

## 📫 Support

For any questions or issues, please open an issue in the GitHub repository.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.