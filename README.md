# Simple Decision Tree on Iris (my notes)

I wanted to understand how decision trees actually pick splits, so I wrote a tiny version from scratch and ran it on the Iris dataset. I only use petal length and petal width so I can draw the decision boundaries and see what the model is doing.

What it does (in short):
- Tries a bunch of thresholds on each feature and picks the one that improves purity the most.
- Grows a small tree up to `max_depth`.
- Prints the rules it learned, the accuracy on the data in the notebook, and a plot of the decision regions.

Files
- [Decision_Tree/iris1.ipynb](Decision_Tree/iris1.ipynb) — the code, training, and plots.
- [Decision_Tree/output.png](Decision_Tree/output.png) — a saved boundary plot (if generated).

How to run it
1. Open the notebook [Decision_Tree/iris1.ipynb](Decision_Tree/iris1.ipynb) in VS Code or Jupyter.
2. Run the cells top to bottom. You should see:
   - A scatter plot of the petal features.
   - Printed rules from the simple tree.
   - An accuracy percentage.
   - A decision boundary figure.

Dependencies
I used `numpy`, `matplotlib`, and `scikit-learn` (just to load Iris). If you need to install them:

```powershell
python -m pip install --upgrade pip
pip install numpy matplotlib scikit-learn
```

A few notes
- This is a learning exercise, not a production tree.
- I kept it to two features to make the plot readable.
- The impurity/gain is simple by design.

If you want more
- Try `sklearn.tree.DecisionTreeClassifier` for a full-featured version (Gini/Entropy, pruning, export, etc.).
- Use all four Iris features and add a proper train/test split.
- Add metrics like precision/recall/F1 to see how it generalizes.
