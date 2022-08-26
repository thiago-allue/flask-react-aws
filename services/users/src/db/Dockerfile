# pull official base image
FROM public.ecr.aws/ubuntu/postgres:latest

# run create.sql on init
ADD create.sql /docker-entrypoint-initdb.d
