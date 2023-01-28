pipeline {
    agent any 
    stages {
        stage('Clone and cleaning') { 
            steps {
                
               
                bat "mvn clean"
            }
        }
        
        stage('static code analytics'){
            steps{
                bat "mvn pmd:pmd"
            }
        }
        
        stage('Checkstyle'){
            steps{
                bat "mvn checkstyle:checkstyle"
            }
        }
       
        stage('Findbugs'){
            steps{
                bat "mvn findbugs:findbugs"
            }
        }
               
        stage('Test') { 
            steps {
                bat "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn install" 
            }
        }
    }
}
