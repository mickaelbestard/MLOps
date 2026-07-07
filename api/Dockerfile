FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*


COPY . .

ENV DATA_PATH=./data/creditcard.csv
ENV MODEL_SAVE_PATH=./model/saved_models/model.pkl

CMD ["python", "model/model.py"]