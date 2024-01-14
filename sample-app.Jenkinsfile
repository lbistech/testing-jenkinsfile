pipeline {
    agent any
    
    stages {
        stage('CopySampleAppCode') {
            steps {
                sh """
                echo '--- Copy website code to /var/www/html ---'
                ls -l
		cp -R sample_application/* /var/www/html/
		ls -l /var/www/html/	
                date
                """
            }
        }
    }
}
