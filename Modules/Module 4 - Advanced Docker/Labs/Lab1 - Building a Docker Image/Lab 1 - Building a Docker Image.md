# Lab 1: Building a Docker Image

In this lab, you will complete the following exercises.

* Create a Dockerfile.
* Build a simple Docker image that runs an Apache web server.
* Pull the image.
* Examine the image on the host OS.

## Prerequisites:
In order to complete this lab, you will need:

* A [Docker Hub](http://www.dockerhub.com) (http://www.dockerhub.com) account. (It's free.)
* An install of [Docker CE](https://www.docker.com/get-started) (https://www.docker.com/get-started). You can run this on any OS. The steps aren't OS-specific.

### Optional: ###
* [Visual Studio Code](https://code.visualstudio.com/download) (https://code.visualstudio.com/download) with the [Docker extension](https://code.visualstudio.com/docs/azure/docker) (https://code.visualstudio.com/docs/azure/docker).

> **Note:** Screenshots in this lab were taken in Visual Studio Code with the Docker extension installed.

---

## Step 1: Create a Dockerfile
You'll need a Dockerfile in order to create a Docker image.

1. Create a directory called **MyDockerApp**.
2. Open a text editor.
3. Add the following to the file.

```
FROM php:7.0.6-apache

COPY apache2.conf /bin/
COPY index.php /var/www/html/
```
3. Save the file in the **MyDockerApp** directory as ``Dockerfile`` with no extension. 

> **Note:** If your text editor has encoder options, make sure that the file is encoded as UTF-8.

4. Copy the ``apache2.conf`` and ``index.php`` files from the 
