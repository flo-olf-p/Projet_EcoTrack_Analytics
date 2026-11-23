FROM python:3.12-slim

WORKDIR /app

COPY . .

RUN python -m venv .venv

RUN . .venv/bin/activate && \
    python -m pip install --upgrade pip && \
    pip install -r requirements.txt && \
    python -c "import sys; print(sys.executable)"

EXPOSE 8000

CMD ["sh", "-c", ". .venv/bin/activate && python app.py"]