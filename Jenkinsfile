pipeline {
    /* specify nodes for executing */
    agent any
    
 
    stages {
        /* checkout repo */
        stage('Checkout SCM') {
            steps {
                checkout([
                 $class: 'GitSCM',
                 branches: [[name: 'master']],
                 userRemoteConfigs: [[
                    url: 'https://github.com/TestingSelenium26/helloworldmaven.git',
                    credentialsId: '',
                 ]]
                ])
            }
        }
         stage('Maven Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
