pipeline {
    agent { label 's1' }
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
				sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
            }
        }
    }
}
