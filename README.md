# Hand-Designed Transformers Implementation

This Jupyter notebook implements a simplified Transformer model from scratch using NumPy and PyTorch, with comparisons between hand-designed and trained models. The project focuses on understanding attention mechanisms through practical implementation and analysis.

## Key Features

### 1. Simplified Transformer Implementation
- **NumPy Version**: Single-layer, single-head Transformer without residual connections or masking
- **PyTorch Version**: Vectorized equivalent model implementing scaled dot-product attention
- Key components: Positional encoding concatenation, query/key/value projections, and softmax attention

### 2. Attention Pattern Analysis
- Identity operation task with one-hot vectors
- Position-aware copying task with custom positional encodings
- Visualization of attention weights and model parameters

### 3. Model Comparisons
- Hand-designed vs. learned attention patterns
- Weight matrix analysis between numpy and PyTorch implementations

## Notebook Structure
1. **Core Components**
   - Helper functions for training loops and model comparison
   - `NumpyTransformer` and `PytorchTransformer` class implementations
   - Gradient-based training loop

2. **Attention Analysis**
   - Content-based attention (identity operation)
   - Position-based attention (copy first token)
   - Side-by-side comparisons of hand-designed vs learned models

3. **Testing Framework**
   - Automated tests for numpy/pytorch equivalence
   - Example test cases for identity and positional tasks

## Results Analysis
Hand-designed vs. learned model comparisons show:
1. **Content Attention**:
   - Similar diagonal attention patterns
   - Learned weights show distributed focus vs hand-designed sparsity

2. **Positional Attention**:
   - Learned models develop position-aware query/key projections
   - Both achieve first-token copying through attention mechanisms

Visualizations demonstrate how learned models often find non-intuitive but effective attention patterns compared to human-designed solutions.
