# Data Cleaning in SQL - README

## Overview

This SQL script demonstrates a series of data cleaning operations performed on the `NashvilleHousing` dataset. The cleaning tasks include standardizing date formats, populating missing property addresses, breaking down address fields, parsing owner addresses, changing values in the "SoldAsVacant" field, removing duplicates, and deleting unused columns.

## Tasks

### 1. Standardize Date Format

- The `SaleDate` column's date format is standardized using the `CONVERT` function.

### 2. Populate Property Address Data

- Missing property addresses are populated by merging data from rows with the same `ParcelID` but different `UniqueID`.

### 3. Breaking Address into Columns (Address, City)

- The `PropertyAddress` column is split into `PropertySplitAddress` and `PropertySplitCity`.

### 4. Parsing Owner Address

- The `OwnerAddress` column is parsed into `OwnerSplitAddress`, `OwnerSplitCity`, and `OwnerSplitState`.

### 5. Change Y and N to Yes and No in "SoldAsVacant" Field

- Values in the `SoldAsVacant` field are updated to "Yes" and "No" accordingly.

### 6. Remove Duplicates

- Duplicate rows are identified using the `ROW_NUMBER()` window function and removed, keeping only one instance of each unique combination of specified columns.

### 7. Delete Unused Columns

- Columns `OwnerAddress`, `TaxDistrict`, `PropertyAddress`, and `SaleDate` are removed as they are no longer needed after data cleaning.

## Execution

- The SQL script should be executed step by step in a database environment where the `PortfolioProject..NashvilleHousing` table exists.

## Note

- Ensure proper database backup before executing delete operations to avoid data loss.

