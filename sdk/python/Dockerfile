FROM public.ecr.aws/docker/library/python:3.11.7-slim

ENV AWS_ACCESS_KEY_ID=
ENV AWS_SECRET_ACCESS_KEY=
ENV AWS_SESSION_TOKEN=
ENV REDSHIFT_PASSWORD=
ENV REDSHIFT_USER=

ADD ./dist/kfp-2.4.0-py3-none-any.whl /kfp-2.4.0-py3-none-any.whl
RUN pip install /kfp-2.4.0-py3-none-any.whl