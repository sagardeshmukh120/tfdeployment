node {
    //def datas = readJSON file: 'config.json'
        
    def buildNumber = env.BUILD_NUMBER
    def workspace = env.WORKSPACE
    def buildUrl = env.BUILD_URL
}
pipeline {
    agent {
        label 'docker-worker'
    }

     stages {      
        stage('Terraform Deployment Build') {

             steps {
                 sh '''
                    echo "Hello"

                 '''

             }
        }
     }
}