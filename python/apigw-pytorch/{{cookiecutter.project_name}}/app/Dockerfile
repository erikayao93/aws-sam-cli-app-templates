FROM public.ecr.aws/lambda/{{cookiecutter.runtime}}

COPY app.py requirements.txt ./
COPY model /opt/ml/model

RUN {{cookiecutter.runtime}} -m pip install -r requirements.txt -t .

CMD ["app.lambda_handler"]
