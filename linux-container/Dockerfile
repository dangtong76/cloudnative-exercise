FROM  ubuntu:20.04

RUN apt-get update \
  && apt install -y wget \
  && apt install -y unzip \
  && apt install -y vim \
  && apt install -y openssh-client \
  && apt install -y curl

 # Download the latest version of Terraform from the official website
 RUN wget https://releases.hashicorp.com/terraform/1.6.6/terraform_1.6.6_linux_arm64.zip

 # Unzip the downloaded file:
 RUN unzip terraform_1.6.6_linux_arm64.zip

 # Move the terraform binary to a directory in your system's PATH.
 RUN mv terraform /usr/local/bin/

 # Verify that Terraform is installed by checking its version:
 RUN terraform version

 # Install awscli for mac
 RUN curl https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip -o awscliv2.zip \
   && unzip awscliv2.zip \
   && ./aws/install \
   && rm -rf aws awscliv2.zip

 # Install awscli for windows
#  RUN curl https://awscli.amazonaws.com/awscli-exe-linux-aarch64.zip -o awscliv2.zip \
#    && unzip awscliv2.zip \
#    && ./aws/install \
#    && rm -rf aws awscliv2.zip


WORKDIR /home
CMD ["bash"]