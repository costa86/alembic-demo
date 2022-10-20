# initial version
alembic revision -m "initial"

# gen model from SQL
sqlacodegen sqlite:///database.db > models.py

# create version
alembic revision --autogenerate -m "initial"

# apply
alembic upgrade head

# sql
    sqlite3 database.db
    sqlite>.schema account


alembic revision --autogenerate -m "add grade"
