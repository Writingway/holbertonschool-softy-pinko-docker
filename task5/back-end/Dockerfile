FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip \
    && rm -rf /var/lib/apt/lists/*

# If the environment is externally managed, remove the marker before using pip
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

RUN pip3 install --no-cache-dir flask flask-cors

WORKDIR /app
COPY api.py /app/
EXPOSE 5252
CMD ["python3", "api.py"]