pipeline{
    agent any
    
    tools {
        maven 'maven-3.8.8'
    }
    
    stages{
        stage('git checkout') {
            
            steps {
                git branch: 'main', credentialsId: 'git_cred', url: 'https://github.com/rakeshbijigi/spring-petclinic.git'
            }
        }
        
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
        
    }
    
}
