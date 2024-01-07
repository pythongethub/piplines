pipeline {
    agent any
    environment {
        name="murali"
        course="k8s"
    }
    stages{
        stage ('env'){
            steps{
                echo "my name is ${name} and i am learning ${course}"

            }
        }
        stage("cred"){
            environment{
                myid=credentials("ssh_murali_creds")
                name="reddy"
            }
            steps{
                echo "my github credentials are ${myid_CREDS}"
                echo "user id: ${myid_USR}"
                echo "password: ${myid_PSW}"
                echo "my name is ${name}"
            }
        }
    }
}
