# Random Number Generation Techniques

This repository contains Python implementations of various random number generation techniques. Each method demonstrates a unique approach to generating pseudo-random numbers, which are useful in simulations, cryptography, and statistical sampling.  

The techniques implemented in this repository include:  

1. **Linear Congruential Method (LCM)**  
2. **Period Calculation for Random Numbers using LCM**  
3. **Combined Congruential Method (CCM)**  
4. **Mid-Square Method**

Below is a detailed explanation of each method, along with the corresponding code and example outputs.  

---

## **1. Linear Congruential Method (LCM)**  

The Linear Congruential Method is one of the simplest and most widely used pseudo-random number generators. The method works based on the following recurrence relation:  

\[ X_{n+1} = (aX_n + c) \mod m \]  

Here:
- \( X \) is the seed or starting value.  
- \( a \) is the multiplier.  
- \( c \) is the increment.  
- \( m \) is the modulus.  

The parameters \( a \), \( c \), and \( m \) should be chosen carefully to ensure good randomness properties and a long period.  


**Output:**  
```
[42, 94, 86, 18, 90, 2, 54, 46, 78, 50]
```

---

## **2. Period Calculation of Random Numbers**  

The period of a random number generator is the number of unique values it produces before repeating itself. This script calculates the period of random numbers generated by the Linear Congruential Method. It checks for repeated values and returns the cycle length.  


**Output:**  
```
Seed:1 - Period:64  
Seed:2 - Period:64  
Seed:3 - Period:64  
```

---

## **3. Combined Congruential Method (CCM)**  

This method enhances randomness by combining two Linear Congruential Generators. The two generators operate independently, and their outputs are combined using the formula:  

\[ Z_n = (X_n + Y_n) \mod M \]  

Where:
- \( X_n \) and \( Y_n \) are outputs of the two generators.  
- \( M \) is the maximum modulus of the two generators.  



---

**Output:**  
```
[2704402962, 2007167484, 589777863, 1054473171, 1866320772, ...]
```

---

## **4. Mid-Square Method**  

This method generates pseudo-random numbers by squaring the seed value and extracting a fixed number of middle digits from the result. The new seed is formed using these middle digits, and the process is repeated.  



---
**Output:**  
```
[5227, 3215, 3362, 3030, 1809, 2724, 4201, 6484, 422, 1780]
```

---
