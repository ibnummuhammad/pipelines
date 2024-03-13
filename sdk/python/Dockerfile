FROM public.ecr.aws/docker/library/python:3.10.13-slim

ENV PLATFORM_ID=kubeflow
ENV REDSHIFT_DATABASE=
ENV REDSHIFT_HOST=
ENV REDSHIFT_IAM=
ENV REDSHIFT_PASSWORD=
ENV REDSHIFT_PORT=
ENV REDSHIFT_USER=
ENV S3_BUCKET=

ADD ./dist/kfp-2.7.0-py3-none-any.whl /opt/kfp-2.7.0-py3-none-any.whl
RUN pip install /opt/kfp-2.7.0-py3-none-any.whl
RUN rm -rf /opt/kfp-2.7.0-py3-none-any.whl

ADD ./dist_ml_pipeline/ml_pipeline-0.8.2-py3-none-any.whl /opt/ml_pipeline-0.8.2-py3-none-any.whl
RUN pip install /opt/ml_pipeline-0.8.2-py3-none-any.whl
RUN rm -rf /opt/ml_pipeline-0.8.2-py3-none-any.whl

RUN pip install boto3==1.27.1
RUN pip install pandas==2.2.1
RUN pip install python-dotenv==1.0.1
RUN pip install redshift-connector==2.1.0
RUN pip install pytz==2024.1
