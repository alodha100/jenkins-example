pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                maven(maven : 'maven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                maven(maven : 'maven') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                maven(maven : 'maven') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
