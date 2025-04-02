# Use Python 3.10 base image
FROM mcr.microsoft.com/devcontainers/python:3.11

# Set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# ENV VIRTUAL_ENV=/opt/venv
# RUN python3 -m venv $VIRTUAL_ENV
# ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# Install system dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Install uv
RUN pip install pipx && pipx ensurepath && pipx install uv && pip install ipykernel

# Set entrypoint
CMD ["bash"]
