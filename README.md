# Bayesian Blocks in R

[![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)](https://www.r-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive R implementation of the Bayesian Blocks algorithm for adaptive histogram generation and data structure discovery.

## 📊 Overview

This repository provides a robust R implementation of the **Bayesian Blocks algorithm**, a sophisticated non-parametric method for creating adaptive histograms that automatically discover and reveal local structure in data. Originally developed by D. Scargle for astronomical time series analysis, this algorithm has proven invaluable across multiple scientific domains.

## 🎯 What is Bayesian Blocks?

The Bayesian Blocks algorithm intelligently segments data intervals into variable-sized blocks based on statistically optimal criteria. Unlike traditional fixed-bin histograms, Bayesian Blocks:

- **Adapts bin sizes** to the local data density
- **Preserves important features** while smoothing noise
- **Optimally partitions data** using Bayesian model selection
- **Reveals hidden structure** that fixed-bin methods might miss

## ✨ Key Features

- 🔧 **Non-parametric approach**: No assumptions about underlying data distribution
- 📈 **Adaptive binning**: Automatically determines optimal bin sizes
- 🎯 **Structure discovery**: Efficiently identifies local patterns and features
- ⚡ **High performance**: Optimized implementation for large datasets
- 📊 **Multiple data types**: Works with time series, spectral data, and general datasets
- 🔬 **Scientific applications**: Tested on real-world scientific datasets
- 📖 **Well-documented**: Comprehensive examples and documentation



## 📊 Example Datasets

This implementation includes several datasets to demonstrate the algorithm's versatility:

### 1. Dummy Dataset
A synthetic dataset combining multiple Gaussian distributions to showcase the algorithm's ability to detect distinct population segments.

### 2. HPGe Detector Spectrum (Eu-152)
Real-world energy spectrum data from a High Purity Germanium detector measuring Europium-152, demonstrating the algorithm's effectiveness in nuclear spectroscopy applications.

```r
# Load and analyze the HPGe spectrum
data("hpge_spectrum")
blocks <- bayesian_blocks(hpge_spectrum$energy, weights = hpge_spectrum$counts)
plot_spectrum_blocks(blocks, hpge_spectrum)
```

## 🔬 Scientific Applications

The Bayesian Blocks algorithm excels in various scientific domains:

- **Astronomy**: Light curve analysis, period detection
- **Nuclear Physics**: Gamma-ray spectroscopy, peak detection
- **Signal Processing**: Change point detection, feature extraction
- **Statistics**: Density estimation, data exploration
- **Economics**: Financial time series analysis

## 📚 Mathematical Foundation

The algorithm uses a fitness function based on Bayesian model comparison:
- Maximizes the posterior probability of block configurations
- Balances model complexity against data fit
- Uses dynamic programming for efficient optimization

## 🎨 Visualization Features

- **Interactive plots** with block boundaries
- **Comparison views** between traditional and Bayesian histograms
- **Customizable styling** for publication-ready figures
- **Export options** for various formats (PNG, PDF, SVG)

## 🧪 Testing

Run the comprehensive test suite:

```r
# Install test dependencies
install.packages("testthat")

# Run tests
devtools::test()
```

## 🤝 Contributing

Contributions are welcome! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on:

- Code style and standards
- Testing requirements
- Documentation expectations
- Pull request process

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📚 References

[1] Scargle, J. D., Norris, J. P., Jackson, B., & Chiang, J. (2013). *Studies in Astronomical Time Series Analysis. VI. Bayesian Block Representations*. The Astrophysical Journal, 764(2), 167.

[2] Pollack, B., et al. (2017). *A Bayesian Blocks Implementation in Python*. arXiv:1708.00810.

[3] Scargle, J. D. (1998). *Studies in Astronomical Time Series Analysis. V. Bayesian Blocks, a New Method to Analyze Structure in Photon Counting Data*. The Astrophysical Journal, 504(1), 405.

[4] Pertoldi, L. (2018). *The Bayesian Blocks algorithm from time series analysis to histogram representation*. GERDA meeting presentation.

## 🙏 Acknowledgments

- Original algorithm development by Jeffrey D. Scargle
- Scientific community for validation and testing
- R community for development tools and best practices



**⭐ If you find this implementation useful, please consider starring the repository!**
