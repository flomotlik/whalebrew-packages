FROM python:latest

RUN pip install 1pass
LABEL io.whalebrew.config.volumes '["~/Dropbox/1Password/:/1Password"]'
ENTRYPOINT ["1pass"]
