# Market-Basket-Analysis
This project demonstrates the application of Market Basket Analysis (MBA) using the Apriori algorithm to find frequent itemsets and generate association rules. The MBA technique helps identify associations and patterns among items frequently purchased together in a transactional dataset.

# Prerequisites
Make sure you have the following dependencies installed:
i) pandas
ii) mlxtend [pip install pandas mlxtend]

# Usage
1. Load the dataset: The dataset should be in CSV format and contain transactional data with columns representing transaction ID, customer ID, date, and item names.
Modify the path in the data = pd.read_csv("<path-to-dataset>") line to specify the path to your dataset.

2. Explore the dataset: This step provides basic information about the dataset, such as the number of rows, column names, data types, and missing values.

3. Data preprocessing: Handle missing values: Any rows with missing values are dropped from the dataset.
Remove duplicates: Duplicate rows are removed to ensure accurate analysis.

4. Data aggregation: Perform data aggregation to group transactions based on the transaction ID, customer ID, and date.
The Itemname column values are aggregated into lists representing the items in each transaction.

5. Generate itemsets: TransactionEncoder is used to transform the list of items in each transaction into a binary matrix.
The Apriori algorithm is then applied to find frequent itemsets in the dataset.

6. Generate association rules: Association rules are generated based on the frequent itemsets using the specified minimum confidence threshold.
The rules are stored in a DataFrame containing antecedents, consequents, support, confidence, and lift.

7. Evaluate and interpret the rules: The generated association rules are printed, displaying the antecedents, consequents, support, confidence, and lift for each rule.

8. Generate recommendations: The get_recommendations function is provided to obtain recommendations based on a set of input items.
Example usages are shown, including filtering association rules, sorting by confidence, and retrieving recommended items.

9. User input for recommendations: The script prompts the user to select input items by their corresponding numbers.
The user can enter the number of input items and then provide the item numbers.
The script returns the recommended items based on the input.

# Additional Notes
The script allows customization of parameters such as the minimum support threshold and minimum confidence threshold.
The dataset used in this example is assumed to be in a specific format. Modify the code accordingly if your dataset has a different structure.

Feel free to customize and adapt the code to suit your specific needs and dataset.
Enjoy exploring market basket analysis and generating valuable recommendations!
