# Using the official Rust image as the base image
FROM rust:latest

#Setting the working directory inside the container to /Backend
WORKDIR /Backend

RUN apt-get update && apt-get -y upgrade && apt-get install -y libpq-dev

COPY . .

RUN cargo install diesel_cli --no-default-features --features postgres

#Copying the run_app.sh script into the container
COPY run_app.sh .

RUN chmod +x run_app.sh

CMD ["./run_app.sh"]
