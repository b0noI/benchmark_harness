
# Start from tensorflow nightly GPU.
FROM tensorflow/tensorflow:nightly-gpu

# File Author / Maintainer
MAINTAINER Toby Boyd

# Update apt-get so latest apps can get installed
RUN apt-get update

# Needed until eng_prod fixed docker nightly to include actual nightly
# added 15-MAR-2018 should not be needed.
RUN pip install --upgrade --force-reinstall https://s3-us-west-2.amazonaws.com/tf-benchmark/tf_binary/tensorflow-1.6.0rc1.6e20f3b_MKL_CUDA9-cp27-cp27mu-linux_x86_64.whl

RUN apt-get -y install --allow-downgrades libcudnn7=7.0.5.15-1+cuda9.0

# Install everything needed via apt-get
RUN apt-get install -y git
RUN pip install --upgrade google-api-python-client pyyaml paramiko google-cloud
