node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'docker-credentials') {

        def customImage = docker.build("tanyawatsepsuk/jenkins-pipeline")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}