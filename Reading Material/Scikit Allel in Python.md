# Scikit-Allel in Python Cheat Sheet 🧬🐍

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Scikit-Allel in Python cheat sheet! Scikit-Allel is a powerful library for analyzing genetic variation data. Whether you're working with DNA sequences or genotyping data, this cheat sheet will guide you through essential concepts and examples.

## Installation

Install Scikit-Allel using pip:

```bash
pip install scikit-allel
```

## Importing Scikit-Allel

Import Scikit-Allel in your Python script or Jupyter notebook:

```python
import allel
```

## Basic Concepts

### 1. Loading Data

Load genetic variation data from various formats:

```python
# Load VCF (Variant Call Format) file
callset = allel.read_vcf('your_file.vcf')

# Load genotype data from HDF5 file
genotypes = allel.read_genotype_hdf5('your_genotypes.h5')
```

### 2. Accessing Variants

Access variant information such as positions and alleles:

```python
# Get variant positions
positions = callset['variants/POS']

# Get variant alleles
alleles = callset['variants/alleles']
```

### 3. Genotype Array

Access and manipulate genotype data:

```python
# Get genotype array
gt = allel.GenotypeArray(callset['calldata/GT'])

# Count alleles per variant
allele_counts = gt.count_alleles()
```

### 4. Filtering Variants

Filter variants based on criteria:

```python
# Filter variants by quality
mask = callset['variants/QUAL'] > 20
filtered_variants = callset.compress(mask, axis=0)
```

### 5. Population Genetics

Compute population genetics statistics:

```python
# Calculate allele frequencies
allele_freqs = gt.count_alleles().to_frequencies()

# Calculate F-statistics
fst_values = allel.stats.fst(gt, your_population_labels)
```

### 6. Plotting

Visualize genetic variation:

```python
# Plot allele frequencies
allel.plot_frequencies(allele_freqs, labels=your_sample_labels)

# Plot PCA (Principal Component Analysis)
allel.plot.pca(gt.to_n_alt(), labels=your_sample_labels)
```

## Advanced Usage

### 7. Distance Matrix

Compute genetic distance matrix:

```python
# Compute genetic distance matrix
dist_matrix = allel.stats.pairwise_distance(gt, metric='euclidean')
```

### 8. Missing Data

Handle missing data:

```python
# Mask missing data
missing_data_mask = gt.is_missing()

# Impute missing data
imputed_gt = gt.impute_with_mean()
```

### 9. Follow the Author

📚 Follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more Python and bioinformatics-related content.

Dive into the world of genetic variation analysis with Scikit-Allel in Python! 🧬🔬💻

Made with :heart: by **Fardeen Ahmad Khan**
