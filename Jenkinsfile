pipeline {
    agent any
    stages {
        stage('Build image') {
            steps {
                echo 'Starting to build docker image'

                script {
                    def customImage = docker.build("hunglm25/sso:${env.BUILD_ID}")
                    docker.withRegistry('https://registry-1.docker.io', 'hunglm25') {
                        customImage.push()
                    }
                    
                }
            }
        }

        stage('Git push') {
            steps {
                echo 'Starting to push new docker image'
                sh 'll'

            }
            }
        }

    }