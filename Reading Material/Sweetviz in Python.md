# Sweetviz in Python Cheat Sheet 🍬🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Sweetviz cheat sheet! Sweetviz is a Python library that helps you visualize and compare dataframes. It's a fantastic tool for exploratory data analysis (EDA) and data comparison. Let's explore Sweetviz with some code examples.

## Installation

You can install Sweetviz using pip:

```bash
pip install sweetviz
```

## Importing Sweetviz

To start using Sweetviz, import it:

```python
import sweetviz as sv
```

## Comparing Dataframes

You can create detailed comparison reports between two dataframes:

```python
# Create dataframes (df1 and df2)
report = sv.compare([df1, "Dataframe 1"], [df2, "Dataframe 2"])
```

## Dataframe Reports

Generate EDA reports for a single dataframe:

```python
report = sv.analyze(df)
report.show_html("report.html")
```

## Show the Report

Display the generated report:

```python
report.show_html("report.html")
```

## Advanced Customization

Sweetviz offers advanced customization options for your reports, including filtering columns, specifying target variables, and more.

## Resources

📖 Official Documentation: [Sweetviz Documentation](https://github.com/fbdesignpro/sweetviz)

Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and data science content. Sweetviz simplifies data exploration and comparison, making your EDA process deliciously easy! 🍬🐍📊

Made with :heart: by **Fardeen Ahmad Khan**
