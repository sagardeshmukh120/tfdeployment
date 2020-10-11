def skipRemainingStages = false
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {

                echo "current build number: ${currentBuild.number}"
                 sh '''
                 echo "current build number:"
                  HOME_PATH="/var/lib/jenkins/workspace/tfdeployment"
                 echo $Number

                 rm -rf ${HOME_PATH}/*

                 rm -rf ${HOME_PATH}/.git

                 #skipRemainingStages = true

                 git clone git@github.com:sagardeshmukh120/envname.git ${HOME_PATH}/new_env/
                 cd ${HOME_PATH}/new_env/

                 sed -i "s/dates=/&$Name,/" ${HOME_PATH}/new_env/file.txt

                 cat file.txt
                 echo "Push the content to newenv to git"
                 git config --global push.default current
                 git remote -v 
                 git status
                 #git add . ; git commit -m "updated " ; git push

                #OldENVCount=`cat file.txt | grep -o -i ${Environment} | wc -l`
                pwd
              
                #web="1"
                #app="5"
                #cls="0"

                #NowebServer=$(((${OldENVCount} * ${web}) + ${web} ))
                ##NoappServer=$(((${OldENVCount} * ${app}) + ${app}))
                #NoclusterServer=$(((${OldENVCount} * ${cls}) + ${cls}))
							
				#VMSize="Standard_D4s_v3"

				#App_code="atg"
                #echo ${Environment} ${VMSize} ${NowebServer} ${NoappServer} ${NoclusterServer} ${App_code} 


                 '''
            }
        }

        stage('Deployment')
        {
            steps{
                    sh '''

                    echo "Deployment Step"

                    '''
            }
        }

        stage('Trigger second pipeline') {

            steps {
                script {
                            echo "the second build pipeline"
                                // echo New_ENV_Name
                            build job: 'secondbuild'
                            
                        }
                            
                }
        }

        stage('After Second Build Trigger')
        {
            steps{
                    sh '''

                    echo "After Second Build Trigger"

                    '''
            }
        }





    }

    
}


