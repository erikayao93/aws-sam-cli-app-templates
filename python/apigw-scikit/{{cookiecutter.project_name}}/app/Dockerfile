FROM public.ecr.aws/lambda/{{cookiecutter.runtime}}

COPY app.py requirements.txt ./
COPY model /opt/ml/model

# temporarily install gcc so that scikit-learn can be built
RUN dnf install gcc-c++ -y

RUN {{cookiecutter.runtime}} -m pip install -r requirements.txt -t .

CMD ["app.lambda_handler"]
