pipeline {
    agent any
    environment {
        NAME = ' RAKSHA '
    }
    stages {
        stage('BUILD') {
            steps {
                echo "$NAME"
                sh '''
                    sleep 5
                    exit 0
                '''
            }
        }
        stage('TEST PARALLEL') {
            parallel {
                stage('TEST ON CHROME') {
                    steps {
                        echo "This is test on Chrome browser"
                        sh 'sleep 5;'
                    }
                }
                stage('TEST ON FIREFOX') {  // Changed this to make parallel stages meaningful
                    steps {
                        echo "This is test on Firefox browser"
                        sh 'sleep 5;'
                    }
                }
            }
        }
    }
}
