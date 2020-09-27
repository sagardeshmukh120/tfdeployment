pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                bash '''#!/bin/bash

                    main
                    function main()
                    {
                        echo "-------------------- Main ----------------------"
                        gitClone
                        TFDestroy
                        TFDeploy
                    }

                    function TFDeploy()
                    {
                        echo "-------------------- TFDeploy ----------------------"
                    }

                    function TFDestroy()
                    {
                        echo "-------------------- TFDestroy ----------------------"
                        AnsibleRole

                    }

                    function gitClone()
                    {
                        echo "-------------------- gitClone ----------------------"

                    }

                    function AnsibleRole()
                    {
                        echo "-------------------- AnsibleRole ----------------------"

                    }

                    



                '''
            }
        }
    }
}