# Assignment-1  
## Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model  

### Dataset
India Air Quality Dataset (NO2 feature used)

---

## Objective

To transform NO2 concentration values using a roll-number-based non-linear transformation and estimate the parameters of a Gaussian-type probability density function.

---

## Step 1: Data Transformation

Each NO2 value \( x \) is transformed into \( z \) using:

z = x + a_r * sin(b_r * x)

Where:

- a_r = 0.05 × (r mod 7)
- b_r = 0.3 × (r mod 5 + 1)
- r = University Roll Number

---

## Step 2: Parameter Estimation

The following probability density function is considered:

p̂(z) = c * exp( -λ (z - μ)^2 )

Parameters estimated:

- μ (mean of transformed variable z)
- λ = 1 / (2σ²)
- c = 1 / √(2πσ²)

Where:
- σ² is the population variance of z

---

## Implementation Details

- Environment: Google Colab
- Libraries used:
  - pandas
  - numpy
  - matplotlib (for visualization)

Steps performed:
1. Loaded dataset
2. Extracted NO2 column
3. Removed missing values
4. Applied transformation
5. Computed mean and variance
6. Calculated λ and c
7. Verified distribution visually using histogram

---

## Final Output

The final submission includes:

- μ
- λ
- c

These values were computed using Maximum Likelihood Estimation for a Gaussian model.

---

## Notes

- Population variance (denominator = n) was used.
- All calculations were performed programmatically.
- Results were verified for consistency.
