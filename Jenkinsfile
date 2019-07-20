pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withEnv(Maven : 'Maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(Maven : 'Maven') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(Maven : 'Maven') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
