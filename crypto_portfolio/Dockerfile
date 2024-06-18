FROM homeassistant/amd64-base-python:latest

# Mettre à jour pip et installer requests
RUN python -m pip install --upgrade pip
RUN pip install requests

COPY run.sh /
COPY crypto_portfolio.py /
COPY db.py /

RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
