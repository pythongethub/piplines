pipeline{
    agent any 
    stages{
        stage ('retry'){
            steps {
                retry(3){
                    echo "hey trying for retry"
                    error "hey its looking fpr error"
                }
                echo "hey after retry"
            }
        }
    }
}
