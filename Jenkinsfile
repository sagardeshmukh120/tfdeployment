pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'

                 main()
            }
        }
    }
}

import java.io.File 
def main(){

    git url: 'https://github.com/sagardeshmukh120/envname.git'
    new File("/var/lib/jenkins/workspace/tfdeployment/file.txt").eachLine {  
         line -> println "line : $line"; 
}
}
