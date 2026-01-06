# Bay Area Public Safety Analytics

This repository contains data analyses of public safety datasets from multiple California cities, including Berkeley, San Francisco, Oakland, and San Jose. The goal of this project is to explore trends in public safety–related data using transparent, reproducible data science methods.

Each subdirectory focuses on a specific city and dataset, and includes exploratory analysis, aggregation, and simple statistical modeling (e.g., regression) to understand how reported incidents or service demand change over time.

## Motivation
Public safety data is widely available through open data portals, but it requires careful interpretation. Different datasets measure different phenomena (e.g., calls for service vs. reported crimes), and trends may reflect changes in reporting behavior, policy, or external events rather than underlying crime rates.

This project emphasizes:
- Asking clear, defensible questions
- Using appropriate aggregation and modeling techniques
- Clearly stating assumptions and limitations

## Structure
bay-area-public-safety-analytics/

├── berkeley/

├── san_francisco/

├── oakland/

├── san_jose/

└── README.md


Each city folder contains:
- One or more Jupyter notebooks with analysis
- A README describing the dataset, question, and findings for that city

## Tools
- Python
- datascience (Berkeley Data 8 module)
- NumPy
- Jupyter Notebooks

## Disclaimer
All datasets used in this repository are publicly available and aggregated. This project is for educational and analytical purposes only and does not make causal claims or policy recommendations.

