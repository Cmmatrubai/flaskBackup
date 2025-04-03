# Flask Backup System with Flutter Frontend

This project implements a backup system with a Flask backend and Flutter frontend. The system allows users to manage and monitor backup operations through a modern, cross-platform interface.

## Project Structure

```
flaskBackup/
├── backend/                 # Flask backend
│   ├── blueprints/         # API route modules
│   ├── venv/              # Python virtual environment
│   ├── app.py             # Main Flask application
│   ├── config.py          # Configuration settings
│   ├── database.py        # Database connection handling
│   ├── requirements.txt   # Python dependencies
│   └── schema.sql         # Database schema
└── frontend/              # Flutter frontend (to be added)
```

## Prerequisites

- Python 3.8 or higher
- Flutter SDK
- MySQL Server
- Git

## Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up the database:
   - Create a MySQL database
   - Import the schema:
     ```bash
     mysql -u your_username -p your_database_name < schema.sql
     ```

5. Configure the application:
   - Update `config.py` with your database credentials and other settings

6. Run the Flask application:
   ```bash
   python app.py
   ```

The backend server will start on `http://localhost:5000`

## Frontend Setup (Flutter)

1. Create a new Flutter project in the frontend directory:
   ```bash
   flutter create frontend
   cd frontend
   ```

2. Add the following dependencies to `pubspec.yaml`:
   ```yaml
   dependencies:
     flutter:
       sdk: flutter
     http: ^1.1.0
     provider: ^6.0.5
     shared_preferences: ^2.2.0
   ```

3. Run `flutter pub get` to install dependencies

4. Configure the API endpoint in your Flutter app to point to the Flask backend

5. Run the Flutter application:
   ```bash
   flutter run
   ```

## API Endpoints

The backend provides the following API endpoints:

- `GET /api/backups` - List all backups
- `POST /api/backups` - Create a new backup
- `GET /api/backups/<id>` - Get backup details
- `DELETE /api/backups/<id>` - Delete a backup

## Development

### Backend Development
- The Flask application uses blueprints for route organization
- Database operations are handled in `database.py`
- Configuration settings are in `config.py`

### Frontend Development
- Follow Flutter best practices for state management
- Use the Provider package for state management
- Implement proper error handling and loading states

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the repository or contact the maintainers. 