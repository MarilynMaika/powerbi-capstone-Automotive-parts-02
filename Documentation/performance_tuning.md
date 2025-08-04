# 🔧 Performance Tuning – Group 3 Project

## 1. Data Model Optimization
- Used star schema layout to improve relationship handling.
- Ensured all relationships used single-direction filters to avoid circular references.


## 2. DAX Optimization
- Replaced calculated columns with measures.

## 3. Visual Performance
- Limited number of visuals per page to reduce rendering load.
- Replaced large tables with summary cards where possible.

## 4. File Size / Load Time
- Ensured numeric columns were cast to correct types (Whole Number, Decimal) to save memory.

## 5. Tools Used
- DAX Studio
