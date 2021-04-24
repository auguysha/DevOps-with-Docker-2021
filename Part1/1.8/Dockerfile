# Start from the ubuntu:18.04 image
FROM ubuntu:18.04

# Use /usr/src/app as the workdir. The following instructions will be executed in this location
WORKDIR /usr/src/app

# Copy the input_website.sh file from this location to /usr/src/app creationg /usr/src/app/inputWebsite.sh
COPY inputWebsite.sh .

# Install the curl package
RUN apt-get update && apt-get install -y curl

# When running docker run the command will be ./inputWebsite.sh
CMD ./inputWebsite.sh
