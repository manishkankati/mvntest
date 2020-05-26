pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat label: '', script: 'mvn compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                   bat label: '', script: 'mvn test'
                }
            }
        }


        stage ('pkg') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    bat label: '', script: 'mvn package'
                }
            }
        }
    }
}
