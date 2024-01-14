pipeline {
    agent any
    parameters {
        string(name: 'FirstName', defaultValue: '', description: 'What is your first name?')
        string(name: 'SecondName', defaultValue: '', description: 'What is your second name?')
        string(name: 'Subject', defaultValue: '', description: 'What is your subject name?')
        string(name: 'Sports', defaultValue: '', description: 'What is your fav sports name?')
        string(name: 'Cert', defaultValue: '', description: 'What is your recent certification name?')
    }
    
    stages {
        stage('User_input') {
            environment {
                FirstName = "${params.FirstName}"
                SecondName = "${params.SecondName}"
                Subject = "${params.Subject}"
                Sports = "${params.Sports}"
                Cert = "${params.Cert}"
            }
            steps {
                sh """
                echo '--- This is my User input script ---'
                /home/ubuntu/scripts/user_input.sh $FirstName $SecondName $Subject $Sports $Cert
                date
                """
            }
        }
    }
}
