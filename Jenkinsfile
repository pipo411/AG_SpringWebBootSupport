pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Building..'
                sh'./gradlew clean assemble' 
            }

            post{
                success{
                    archiveArtifacts artifacts: 'build/libs/*.jar', fingerprint: true
                }
            }

        }
        stage('Example') {
            steps {
                echo 'Building..'
                sh'./gradlew test'
            }

            post{
                success{
                   echo 'Paso'
                }
            }

        }
    }
}


