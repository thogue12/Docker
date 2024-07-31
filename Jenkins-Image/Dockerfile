FROM jenkins/jenkins:lts

USER root

# Install curl and unzip
RUN \
    apt-get update && \
    #Install unzip
    apt-get install -y curl unzip wget awscli
    

# Install Terraform
RUN \
    wget https://releases.hashicorp.com/terraform/1.9.3/terraform_1.9.3_linux_amd64.zip && \
    unzip terraform_1.9.3_linux_amd64.zip && \
    mv terraform /usr/local/bin/ && \
    rm terraform_1.9.3_linux_amd64.zip && \
    terraform --version

# Verify AWS CLI

RUN aws --version

#expose jenkins port
EXPOSE 8080
EXPOSE 5000

USER jenkins

