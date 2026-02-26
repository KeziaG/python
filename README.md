# Python Project with pyodbc

This is a Python project with pyodbc installed for database connections.

## Setup Instructions

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/KeziaG/python.git
cd python
```

2. Create a virtual environment:
```bash
python -m venv venv
```

3. Activate the virtual environment:
   - On Windows:
   ```bash
   venv\Scripts\activate
   ```
   - On macOS/Linux:
   ```bash
   source venv/bin/activate
   ```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Once installed, you can use pyodbc to connect to databases:

```python
import pyodbc

# Example connection string
connection_string = 'Driver={ODBC Driver 17 for SQL Server};Server=YOUR_SERVER;Database=YOUR_DB;UID=YOUR_USER;PWD=YOUR_PASSWORD'
conn = pyodbc.connect(connection_string)
cursor = conn.cursor()

# Execute queries
cursor.execute('SELECT * FROM your_table')
for row in cursor.fetchall():
    print(row)

conn.close()
```

## Dependencies

- **pyodbc** - Python ODBC bridge for database connectivity

## License

MIT