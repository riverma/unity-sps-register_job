FROM ghcr.io/unity-sds/unity-sps-prototype/sps-hysds-pge-base:develop

USER root

# Accept environment variables as build parameters
ARG STAGING_BUCKET
ARG CLIENT_ID
ARG DAPA_API
ARG JOBS_DATA_SNS_TOPIC_ARN

# Set environment variables
ENV STAGING_BUCKET=${STAGING_BUCKET}
ENV CLIENT_ID=${CLIENT_ID}
ENV DAPA_API=${DAPA_API}
ENV JOBS_DATA_SNS_TOPIC_ARN=${JOBS_DATA_SNS_TOPIC_ARN}

# TODO: change entrypoint, since we will not be running a bash script
ENTRYPOINT ["/cwl/run_cwl_workflow.sh"]
