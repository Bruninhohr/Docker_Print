FROM python:3.11-slim

COPY Pipfile Pipfile.lock ./

RUN python -m pip install --upgrade pip

RUN pip install pipenv && pipenv install --dev --system --deploy

WORKDIR /app

COPY /app/mlops_puc.py /app

CMD ["python","-u","mlops_puc.py"]