FROM public.ecr.aws/lambda/python:3.12

# Copy testing.txt
COPY testing.txt ${LAMBDA_TASK_ROOT}

# Install the specified packages
RUN pip install -r testing.txt

# Copy function code
COPY app.py ${LAMBDA_TASK_ROOT}

# Set the CMD to your handler (could also be done as a parameter override outside of the Dockerfile)
CMD [ "app.handler" ]
