# stage 1 : build stage
FROM python:3.10-slim as builder

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# final stage
FROM python:3.10-slim

WORKDIR /app

COPY *.py . 

COPY --from=builder /app ./

EXPOSE 5000

CMD ["python", "app.py"]
