# Containers
- A container organizes a set of blobs, similar to a directory in a file system.
- A storage account can include an unlimited number of containers, and a container can store an unlimited number of blobs.
- A container name must be a valid DNS name, as it forms part of the unique URI (Uniform resource identifier) used to address the container or its blobs.
- Follow these rules when naming a container:
    - Container names can be between 3 and 63 characters long.
    - Container names must start with a letter or number, and can contain only lowercase letters, numbers, and the dash (-) character.
    - Two or more consecutive dash characters aren't permitted in container names.

- The URI for a container is similar to: https://myaccount.blob.core.windows.net/mycontainer