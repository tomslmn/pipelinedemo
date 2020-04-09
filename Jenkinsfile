pipeline {
    agent any
    stages {
        stage('Build Application') {
          
            steps {
               bat 'mvn clean install'
            }
        }
        stage('Test Application') {
            
            steps {
               bat 'mvn clean test'
            }
        }
        stage('Deploy Application') {
            
            steps {
              bat 'mvn clean package deploy -Dmule.version=4.2.2 -Dusername=tommamo -Dpassword=17297@Mule -Denvironment=Sandbox -Dworkers=1 -Dworker.type=MICRO -Dapplication.name=hello -DmuleDeploy'

           }
       }
    }
}