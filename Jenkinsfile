pipeline {
    agent any 
    stages {
        stage('Build Application') { 
            steps {
                
                bat "mvn clean install"
            }
        }
        stage('Test') { 
            steps {
              bat "mvn clean test" 
            }
        }
        stage('Deploy') { 
            steps {
             bat "mvn clean package deploy -Dmule.version=4.2.2 -Dusername=tigist -Dpassword=Ethiopia1@ -Dworkers=1 -Dworker.type=Micro -Denvironment=Sandbox -Dapplication.name=today"
            }
        }
    }
}