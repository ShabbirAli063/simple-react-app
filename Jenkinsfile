pipeline {
    agent {
        
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}


dbpass:'acdefgtdbsge'
accesskey=NKJAKASLNLANFLSNLFNNCLNSLKANL
secretkey=5cwd6BdnGHJ76BHBBbkkd8jhbbdBBTFY
