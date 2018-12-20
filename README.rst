TeamCity Docker Agent with Docker-in-Docker sidecar
===================================================

This project is an example of how to run the TeamCity Agent with Docker running in a separate sidecar container. This is an alternative to the method used by the `official Teamcity Agent Docker image <https://hub.docker.com/r/jetbrains/teamcity-agent>`_, which runs Docker inside the same container as the Agent.

Advantages
----------

* Easily customise Docker daemon options available in the official `Docker-in-Docker image <https://hub.docker.com/_/docker>`_
* Use a Docker version that is different from the one bundled in the TeamCity Agent image
* Stop & upgrade the Docker sidecar without Agent downtime
* Separation of concerns between Docker containers

Usage
-----

To start up the containers:

.. code-block:: sh

	docker-compose up

To stop the containers and remove all volumes:

.. code-block:: sh

	docker-compose down --volumes
