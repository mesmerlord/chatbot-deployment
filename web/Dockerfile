FROM python:3.7-slim-buster

COPY . /
RUN pip3 install --upgrade setuptools pip
RUN pip3 install -r requirements.txt
RUN pip3 install torch==1.10.1+cpu torchvision==0.11.2+cpu torchaudio==0.10.1+cpu -f https://download.pytorch.org/whl/cpu/torch_stable.html
RUN python3 start.py
RUN python3 train.py
RUN chmod +x /runserver.sh
ENTRYPOINT ["/runserver.sh"]