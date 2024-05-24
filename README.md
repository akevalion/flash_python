# flask_python
Just fun
# Install steps
- Install Docker
- Use the `docker-compose.yml` file with the configurations to create PostgreSQL container
- Start PostgreSQL with docker compose up
```
docker-compose up
```
- Identify the PostgreSQL container ID with the following command:
```
docker ps
```
- Then, execute the shell, this case the id is:
```
docker exec -it 2fbbea63cefd bash
```
- Previously create the database in PostgreSQL
```
psql -U admin;
create database demo;
\l;
exit;
```
- In the working directory, activate the virtual environment
```
pip install virtualenv
venv\Scripts\Activate.ps1
flask shell 
from app import db
db.create_all()
quit()
```
- Start the project with `python app.py`
