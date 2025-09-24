# Helio App - Shared Database Configuration

## Database Details
- **Database Name**: helio
- **Password**: Ashrudi
- **Type**: SQLite (shared across all modules)

## Modules
- **Doctor**: `/doctor/backend/` - Doctor portal backend
- **Patient**: `/patient/backend/` - Patient portal backend  
- **Pharmacist**: `/pharmacist/backend/` - Pharmacy management backend

## Database Location
The shared database file should be located at the root level or each module should point to the same database instance.

## Configuration Files to Update
1. `/doctor/backend/.env` or `/doctor/backend/config.py`
2. `/patient/backend/.env` or `/patient/backend/config.py`
3. `/pharmacist/backend/config.py`

Make sure all three modules use:
```
DATABASE_NAME=helio
DATABASE_PASSWORD=Ashrudi
```