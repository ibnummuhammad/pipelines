FROM public.ecr.aws/docker/library/python:3.11.7-slim

ENV DATA_AWS_ACCESS_KEY_ID=
ENV DATA_AWS_SECRET_ACCESS_KEY=
ENV DATA_AWS_SESSION_TOKEN=
ENV ENGINEERING_AWS_ACCESS_KEY_ID=
ENV ENGINEERING_AWS_SECRET_ACCESS_KEY=
ENV ENGINEERING_AWS_SESSION_TOKEN=
ENV PLATFORM_ID=kubeflow
ENV REDSHIFT_PASSWORD=
ENV REDSHIFT_USER=

ADD ./dist/kfp-2.7.0-py3-none-any.whl /opt/kfp-2.7.0-py3-none-any.whl
RUN pip install /opt/kfp-2.7.0-py3-none-any.whl
RUN rm -rf /opt/kfp-2.7.0-py3-none-any.whl

ADD ./dist_ml_pipeline/ml_pipeline-0.4.3-py3-none-any.whl /opt/ml_pipeline-0.4.3-py3-none-any.whl
RUN pip install /opt/ml_pipeline-0.4.3-py3-none-any.whl
RUN rm -rf /opt/ml_pipeline-0.4.3-py3-none-any.whl

RUN pip install boto3==1.27.1
RUN pip install pandas==2.2.1
RUN pip install python-dotenv==1.0.1
RUN pip install redshift-connector==2.1.0
