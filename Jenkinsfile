pipeline
{

        agent any
         stages {
                stage('Pull') {
                    steps {
                        script {
                         checkout([$class: 'GitSCM' , branches: [[name: '*/main']],
                                userRemoteConfigs: [[
                                        credentialsId: '7401739f-86aa-4aeb-939d-9689719edb2b',
                                        url: 'https://github.com/MedLadhibi/ProjetCD.git' ]]])


                                }
                          }
                                }
                stage('Build') {
		    steps {
			script {
			sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml"

				}
			}
				}

                stage('docker') {
                    steps{
                        script{
                        sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml"
                                }
                        }
                                }

 }
}

