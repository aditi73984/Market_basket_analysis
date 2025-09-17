Market Basket Analysis

This project performs **Market Basket Analysis** on a retail dataset using the
FP-Growth algorithm and visualizes strong association rules as a network graph.

## 📂 Project Files
- `Dataset.csv` – Input data: each row is a transaction (items separated by commas, no header).
- `market_basket_analysis.py` – Main Python script with all processing steps.
- `association_rules.csv` – Generated association rules with metrics.
- `frequent_itemsets.csv` – Frequent itemsets with their support values.

## 🛠️ Requirements
- Python 3.8+
- Packages: `pandas`, `mlxtend`, `matplotlib`, `networkx`



## ▶️ How to Run

1. Place your transactions in `Dataset.csv` (one basket per row).
2. Run the script:

   python market_basket_analysis.py
  
3. Output:

   * Frequent itemsets and association rules saved as CSV files.
   * A pop-up network graph of the top association rules.

## ⚡ Key Steps in the Script

1. **Load Data**: Read `Dataset.csv` and convert each row to a list of items.
2. **One-Hot Encode**: Transform transactions into a sparse Boolean matrix.
3. **Frequent Itemsets**: Use FP-Growth (`fpgrowth`) to find itemsets above `min_support`.
4. **Association Rules**: Generate rules with `association_rules` using confidence ≥ 0.3.
5. **Visualization**: Plot a network where nodes are items and edges are rules, weighted by lift.

## 🔧 Adjustments

* **Minimum Support/Confidence**: Edit `min_support` in `fpgrowth` and `min_threshold` in `association_rules` for more or fewer rules.
* **Graph Size**: Change `top_n` parameter in `plot_rule_graph` to show more/less rules.

## 📜 Example Output

* Frequent itemsets like `("mineral water")` with their support.
* Rules such as `{herb & pepper} → {ground beef}` with confidence, lift, etc.

**Author:** Aditi

```
