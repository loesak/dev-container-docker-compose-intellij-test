FROM ubuntu:22.04

# Create the user
ARG USERNAME=devenv
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Create the user
RUN groupadd --gid $USER_GID $USERNAME \
    && useradd --uid $USER_UID --gid $USER_GID -m $USERNAME

# Create workspace directory and change ownership
RUN mkdir -p /workspace && chown $USERNAME:$USERNAME /workspace

# Set the default user
USER $USERNAME
WORKDIR /workspace
