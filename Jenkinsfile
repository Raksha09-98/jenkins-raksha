pipeline {
    agent {
        label 'new-label' // Specify the label of the slave node where you want to run the job
    }
    stages {
        stage('BUILD') {
            steps {
                echo "This is build stage"
                sh '''
                    sleep 5
                    exit 0
                '''
            }
        }
    }
}
