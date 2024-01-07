pipeline{
    agent any
    stages{
        stage{
            steps{
                echo "deploying to dev eni successfully"
            }
        }
        stage{
            options{
                timeout(time:300,unit:'SECONDS')
            }
            input{
                message "should we  continue ???"
                ok "Approved"
                submitter "muralidhar"
                submitterParameter "whoApproved"
                parameters{
                    string(name:'CHANGE_TICKET', defaultValue: 'CH12345',description: 'Please Enter Change Ticket number')
                    booleanParam(name: 'SRE Approved ????', defaultValue: true, description: 'Is approval taken from SRE??')
                    choice(name: 'Release', choices: 'Regular\nHotfix', description: 'What type of release is this ??')
                    text(name: 'Notes', defaultValue: "Enter release notes if any.....", description: 'Release Notes')
                    password(name: 'myPassword', defaultValue: 'myPasswordValue', description: 'Enter the password')
                    credentials(name: 'myCredentials', description: 'My Credentials stored', required: true)
                }
            }
            steps{
                steps {
                echo "The Change Ticket is ${CHANGE_TICKET}"
                echo "Deploying to Production"
                echo "This is a ${Release} Release"
                echo "Approved by ${whoApproved}"
            }
        }
    }
}
}
