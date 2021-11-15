pipeline
{

        angent any
         stages {
                stage('Pull') {
                    steps {
                        script {
                         checkout([$class: 'GITSCM' , branches: [[name: "*/main"]],
                                userRemoteConfigs: [[
                                        credentialsId: '7401739f-86aa-4aeb-939d-9689719edb2b',
                                        url: 'https://github.com/MedLadhibi/ProjetCD.git ]]])


                                }
                          }
                                }
                 }
}

