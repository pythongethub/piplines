pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                retry (3) {
                    timeout(time:2, unit:'SECONDS'){
                        echo "Welocme to Pipeline"
                        error "Testing the Retry block"
                    }
                }
                echo "Printing after 3 retrys"
            }
        }
    }
}
