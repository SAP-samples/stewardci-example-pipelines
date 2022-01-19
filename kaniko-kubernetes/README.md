# Docker Build in Kubernetes with Kaniko

Run a pod in Kubernetes that executes Kaniko performing a Docker build.

-   Kaniko runs with UID/GID 0 (root).

    Note that Kubernetes security settings, e.g. the used Pod Security Policy,
    must allow for using UID/GID 0.

-   The first stage of the Docker build runs as user root.
    It performs operations that require root (update apt package database,
    install new package).

-   The second stage of the Docker build starts off as user 1000, and
    runs a command via sudo.
