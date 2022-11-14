pipeline {
    agent any
    stages {
        stage ("Pull") {
            steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    userRemoteConfigs:[[
                        credentialsId: 'github', 
                           url: 'https://github.com/Mabrouka-Chebbi/Project.git']]])
                }
            }
        }

       
	stage('Build'){
            steps{
                script{
                 sh " ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml "
                }
            }
        }

       stage('docker'){
            steps{
                script{
                    echo "hello"
                }
            }
        }
        stage('docker-registry'){
            steps{
                script{
                    echo "hello"
                }
            }
        }







            
         }
         
         }
