pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'

                 sh '''
                  HOME_PATH="/var/lib/jenkins/workspace/tfdeployment"
                 echo $Number

                 git clone https://github.com/sagardeshmukh120/envname.git ${HOME_PATH}/new_env/
                 cd ${HOME_PATH}/new_env/
                OldENVCount = `cat file.txt | grep -o -i ${Environment} | wc -l`
                pwd
              
				NowebServer = `expr ($OldENVCount * 1) + 1`
				NoappServer = `expr ($OldENVCount * 5) + 5`
				NoclusterServer = `expr ($OldENVCount * 0) + 0`
							
				VMSize="Standard_D4s_v3"

				App_code="atg"
                echo ${Environment} ${VMSize} ${NowebServer} ${NoappServer} ${NoclusterServer} ${App_code} 


                 '''
            }
        }
    }
}


