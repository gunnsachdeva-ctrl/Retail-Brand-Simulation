# Retail-Brand-Simulation
Simulation-based retail demand model in R modeling 1,000 heterogeneous consumers across 3 SKUs and 5 channels using price elasticity, advertising response, and multinomial logit choice modeling.
Problem Statement
Modern retail firms sell multiple products across different channels and invest in advertising across multiple media platforms. However, customer responses to price changes and advertising exposure are not uniform.

This project aims to simulate a retail market with three SKUs (elastic, inelastic, and moderately elastic) sold across five sales channels (Website, Amazon, and three physical stores) and advertised across three media channels (Web, TV, Print).
The objective is to model how heterogeneous consumers with varying price sensitivity and advertising responsiveness make purchase decisions, and to evaluate the impact of elasticity and advertising intensity on sales, revenue, and channel performance.


 #Methodology
Demand Curve Construction

Each SKU follows a linear demand function:

Q=a−bP

where b represents price elasticity.


Advertising Response Function
Demand is adjusted using a logarithmic advertising lift function to reflect diminishing returns:

Boost=1+γ⋅log(1+intensity)

Random-Coefficient (Heterogeneous) Consumer Modeling

1,000 synthetic customers are generated.

Each customer receives randomly jittered:

Product preference (intercept)

Price sensitivity (elasticity)

Advertising responsiveness (γ)

Utility & Choice Modeling

For each customer, utility is computed for all SKU × channel combinations.
Utilities are converted to choice probabilities using the Softmax (Multinomial Logit) model, including an outside option.


Purchase Simulation

Customer choices are simulated probabilistically, generating:

SKU-level demand

Channel-level sales

Revenue outcomes

Conversion rates


Visualization & Diagnostics

Elasticity distributions, ad responsiveness, and purchase outcomes are visualized to validate model behavior.

Tools Used
R – Core modeling and simulation

tidyverse – Data manipulation

ggplot2 – Data visualization

dplyr – Data transformation

readr – Output generation

Multinomial Logit (Softmax implementation) – Choice modeling


Key Results

Demonstrated impact of price elasticity on SKU-level sales

Modeled diminishing returns of advertising across media channels

Simulated heterogeneous consumer behavior using random coefficients

Generated synthetic dataset of 1,000 purchase decisions

Evaluated channel performance and revenue distribution

Showed realistic probabilistic choice behavior using multinomial logit
