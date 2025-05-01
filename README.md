# Handwritten Mathematical Expression Recognition

This project implements a complete pipeline for recognizing, parsing, and evaluating handwritten mathematical expressions from images.

## Overview

We developed a robust system that:
- Uses a CNN-based classifier to recognize handwritten math symbols.
- Applies contour-based segmentation to extract symbols from full equations.
- Reconstructs the structure of expressions using a rule-based layout-aware parser.
- Evaluates expressions symbolically to solve equations.

## Key Features

- **CNN Classifier**: Achieves 98.97% accuracy on a test set of 81 symbol classes.
- **Vision Transformer (ViT)**: Used for performance comparison.
- **Contour-based Segmentation**: For symbol detection in full equation images.
- **Rule-Based Parser**: Converts spatial symbol arrangements into valid LaTeX/math expressions.
- **Symbolic Solver**: Computes solutions to parsed math expressions.

## Dataset

- **Source**: [Kaggle - Handwritten Math Symbols](https://www.kaggle.com/datasets/xainano/handwrittenmathsymbols)
- ~100,000 grayscale images across 81 classes.
- Input size: 45x45 pixels, with adaptive binarization and class-specific augmentations.

## Results

- CNN classifier outperforms baseline models with 98.97% accuracy.
- ViT shows similar accuracy but is computationally heavier.
- Successful end-to-end reconstruction and evaluation of expressions (e.g., solving `x^2 - 9 = 0` to get `x = ±3`).

