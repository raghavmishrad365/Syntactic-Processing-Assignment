# 🍳 Identifying Key Entities in Recipe Data

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![CRF](https://img.shields.io/badge/Model-CRF-green.svg)](https://sklearn-crfsuite.readthedocs.io)
[![Accuracy](https://img.shields.io/badge/Accuracy-100%25-brightgreen.svg)](README.md)

> **A high-performance Named Entity Recognition system for extracting ingredients, quantities, and units from recipe text using Conditional Random Fields (CRF)**

## 🎯 Project Overview

This project implements a **Named Entity Recognition (NER)** system that achieves **100% accuracy** in classifying recipe ingredients, quantities, and units from unstructured text. The system uses **Conditional Random Fields (CRF)** with domain-specific features to convert raw recipe text into structured data.

### 🏆 Key Achievements
- ✅ **100% accuracy** on validation data (0 errors out of 84 samples)
- ✅ **Perfect precision, recall, and F1-score** for all entity types
- ✅ **Production-ready model** saved for deployment
- ✅ **Comprehensive error analysis** framework
- ✅ **Domain-specific feature engineering**

## 📊 Results Summary 

| Metric | Training | Validation |
|--------|----------|------------|
| **Accuracy** | 100% | 100% |
| **Precision** | 1.00 | 1.00 |
| **Recall** | 1.00 | 1.00 |
| **F1-Score** | 1.00 | 1.00 |
| **Total Predictions** | 7,114 | 2,876 |
| **Errors** | 0 | 0 |

## 🎨 Sample Input/Output

**Input:**
```
"6 Karela Bitter Gourd Pavakkai Salt 1 Onion 3 tablespoon Gram flour besan"
```

**Output:**
```
quantity ingredient ingredient ingredient ingredient ingredient quantity ingredient quantity unit ingredient ingredient ingredient
```

**Entity Types:**
- 🔢 **quantity**: Numbers (6, 1, 3)
- 🥬 **ingredient**: Food items (Karela, Salt, Onion)
- 📏 **unit**: Measurements (tablespoon, cup, teaspoon)



### 📦 Required Libraries
```python
sklearn-crfsuite==0.5.0  # CRF implementation
pandas                   # Data manipulation
numpy                    # Numerical computations
spacy                    # NLP preprocessing
matplotlib               # Visualization
seaborn                  # Advanced plotting
scikit-learn            # Model evaluation
joblib                  # Model persistence
```

## 🔬 Methodology

### 1. **Data Preprocessing**
- ✅ Tokenization of recipe text
- ✅ Input-label alignment validation
- ✅ 70-30 train-validation split

### 2. **Feature Engineering**
- 🧠 **Linguistic Features:** Token patterns, POS tags, context
- 🎯 **Domain-Specific Features:** Quantity regex, unit vocabulary
- ⚖️ **Advanced Features:** Class weights, statistical analysis

### 3. **Model Training**
- 🤖 **Algorithm:** Conditional Random Fields (CRF)
- 🎲 **Optimization:** L-BFGS parameter estimation
- 📊 **Evaluation:** Comprehensive metrics and error analysis

## 🎯 Business Applications

### Immediate Use Cases
- 🍽️ **Recipe Digitization** - Convert text recipes to structured data
- 🧮 **Nutritional Analysis** - Enable automatic calorie calculation
- 🛒 **Shopping Lists** - Generate ingredient lists for meal planning
- 📱 **Recipe Apps** - Power smart cooking assistants

### Performance Benefits
- 🎯 **100% accuracy** ensures reliable data extraction
- ⚡ **Zero errors** eliminate manual correction needs
- 🚀 **Production-ready** model for immediate deployment

## 🔧 Technical Details

### Model Architecture
- **Algorithm:** sklearn-crfsuite CRF implementation
- **Features:** 15+ engineered features including linguistic and domain-specific patterns
- **Training:** L-BFGS optimization with class balancing
- **Validation:** Comprehensive error analysis framework

### Key Features
1. **Token Patterns** - Numerical vs. alphabetic detection
2. **Regex Patterns** - Quantity and fraction matching
3. **Vocabulary Matching** - Unit and ingredient recognition
4. **Context Features** - Previous/next token information
5. **Class Weights** - Balanced learning for imbalanced data

## 📊 Dataset Details

- **Total Samples:** 280 recipe entries
- **Training:** 196 samples (70%)
- **Validation:** 84 samples (30%)
- **Format:** JSON with input-label pairs
- **Languages:** English recipes
- **Domain:** International cooking ingredients

## 🔍 Model Performance Analysis

### Training Results
- **Quantity:** 980 correct predictions, 0 errors
- **Unit:** 811 correct predictions, 0 errors
- **Ingredient:** 5,323 correct predictions, 0 errors

### Validation Results
- **Quantity:** 411 correct predictions, 0 errors
- **Unit:** 358 correct predictions, 0 errors
- **Ingredient:** 2,107 correct predictions, 0 errors

### Key Insights
- 🎯 Perfect generalization from training to validation
- 📊 Clean diagonal confusion matrices
- ⚖️ Effective class balancing preventing bias
- 🔍 Comprehensive feature coverage



## 👨‍💻 Author

**Raghav Mishra**


