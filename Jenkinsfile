pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                retry (3) {
                    echo "Welocme to Pipeline"
                    error "Testing the Retry block"
                }
                echo "Printing after 3 retrys"
            }
        }
    }
}
