# Use Ubuntu 20.04 as the base image
FROM ubuntu:20.04

# Install Squid and other necessary packages
RUN apt-get update && apt-get install -y squid

# Copy the Squid configuration file
COPY squid.conf /etc/squid/squid.conf

# Expose the port (optional, since Render uses the PORT environment variable)
EXPOSE ${PORT}

# Start Squid in the foreground
CMD ["squid", "-N"]
