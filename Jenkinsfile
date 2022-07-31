node {
    stage("check file"){
        sh ''' ls '''
    }
    stage("1"){
        sh ''' ls '''
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'docker-credentials') {

        def customImage = docker.build("tanyawatsepsuk/jenkins-pipeline")

        /* Push the container to the custom Registry */
        customImage.push()
    }
    }


}