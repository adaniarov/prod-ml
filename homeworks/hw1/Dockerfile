FROM python:3.12-slim-bookworm
RUN pip install uv
WORKDIR /app
COPY pyproject.toml uv.lock .python-version ./
RUN uv sync 
COPY Dockerfile app.py ./

CMD ["uv", "run", "python", "app.py"]