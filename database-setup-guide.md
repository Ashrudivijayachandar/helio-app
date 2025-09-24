# Database Configuration Update Script

This script helps update all three modules to use the shared "helio" database with password "Ashrudi".

## Files to Update:

### 1. Doctor Module Database Configuration
**File**: `doctor/backend/.env` or `doctor/backend/config.py`
**Update**: Set database name to "helio" and password to "Ashrudi"

### 2. Patient Module Database Configuration  
**File**: `patient/backend/.env` or `patient/backend/config.py`
**Update**: Set database name to "helio" and password to "Ashrudi"

### 3. Pharmacist Module Database Configuration
**File**: `pharmacist/backend/config.py`
**Update**: Set database name to "helio" and password to "Ashrudi"

## Example Configuration:

For Python Flask apps, update the database URI:
```python
SQLALCHEMY_DATABASE_URI = 'sqlite:///helio.db'
# or for other databases:
# SQLALCHEMY_DATABASE_URI = 'postgresql://username:Ashrudi@localhost/helio'
```

For .env files:
```
DATABASE_NAME=helio
DATABASE_PASSWORD=Ashrudi
```

## Verification Steps:
1. Ensure all three modules can connect to the same database
2. Test that data is shared between modules
3. Verify that user authentication works across all portals
4. Check that appointments, prescriptions, and inventory are synchronized