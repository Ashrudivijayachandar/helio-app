# Helio App - Healthcare Management Monorepo

A comprehensive healthcare management system with separate modules for doctors, patients, and pharmacists, all sharing the same database.

## 🏗️ Repository Structure

```
helio-app/
├── doctor/           # Doctor portal
│   ├── backend/      # Doctor backend API
│   ├── frontend/     # Doctor React frontend
│   └── instance/     # Doctor instance data
├── patient/          # Patient portal
│   ├── backend/      # Patient backend API
│   ├── frontend/     # Patient React frontend
│   └── instance/     # Patient instance data
├── pharmacist/       # Pharmacy management
│   ├── backend/      # Pharmacy backend API
│   ├── frontend/     # Pharmacy React frontend
│   ├── mobile-app/   # Pharmacy mobile app
│   └── database/     # Database schemas
├── database-config.md # Shared database configuration
└── README.md         # This file
```

## 🗄️ Shared Database

All three modules use the same database:
- **Database Name**: `helio`
- **Password**: `Ashrudi`
- **Type**: SQLite (or your preferred database)

## 🚀 Getting Started

### Prerequisites
- Node.js (for React frontends)
- Python 3.x (for Flask/Python backends)
- SQLite (or your preferred database)

### Setup Instructions

#### 1. Clone the Repository
```bash
git clone https://github.com/Ashrudivijayachandar/helio-app.git
cd helio-app
```

#### 2. Set up Doctor Module
```bash
cd doctor/backend
pip install -r requirements.txt
# Configure database connection to use "helio" database

cd ../frontend
npm install
npm start
```

#### 3. Set up Patient Module
```bash
cd patient/backend
pip install -r requirements.txt
# Configure database connection to use "helio" database

cd ../frontend
npm install
npm start
```

#### 4. Set up Pharmacist Module
```bash
cd pharmacist/backend
pip install -r requirements.txt
# Configure database connection to use "helio" database

cd ../frontend
npm install
npm start
```

## 🔧 Configuration

Each module should be configured to use the shared database:

### Backend Configuration
Update the database configuration in each backend:
- `doctor/backend/.env` or `doctor/backend/config.py`
- `patient/backend/.env` or `patient/backend/config.py`
- `pharmacist/backend/config.py`

Ensure all use:
```
DATABASE_NAME=helio
DATABASE_PASSWORD=Ashrudi
```

## 📱 Module Features

### Doctor Portal (`/doctor/`)
- Patient management
- Appointment scheduling
- Medical consultations
- Analytics and reports

### Patient Portal (`/patient/`)
- Appointment booking
- Medical history
- Medicine tracking
- Communication with doctors

### Pharmacist Portal (`/pharmacist/`)
- Inventory management
- Prescription processing
- Medicine stock tracking
- Rare medicine handling
- Mobile app support

## 🌐 Development

### Running All Modules
You can run each module independently on different ports:
- Doctor frontend: typically `http://localhost:3000`
- Patient frontend: typically `http://localhost:3001`
- Pharmacist frontend: typically `http://localhost:3002`

### Backend APIs
- Doctor API: typically `http://localhost:5000`
- Patient API: typically `http://localhost:5001`
- Pharmacist API: typically `http://localhost:5002`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔗 Original Repositories

This monorepo was created by merging:
- [helio-pharmacy](https://github.com/Ashrudivijayachandar/helio-pharmacy) → `/pharmacist/`
- [Helio-demo](https://github.com/gsribarath/Helio-demo) → `/doctor/` and `/patient/`

## 📞 Support

For support, please contact the development team or open an issue in this repository.