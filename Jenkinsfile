pipeline {
  agent any
  stages {
    stage('pull') {
      steps {
        script {
          checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                  userRemoteConfigs: [[
                      credentialsId: 'AngApp',
                      url: 'https://github.com/AlaaEddineBoukhriss/AngApp.git'
                    ]
                  ]
                ])
            }
          }
        }
    stage('build ') {
      steps { 
        script{ 
          sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
        }
      }
    }
     stage('Build Docker Img ') {
            steps {
                script{
                    sh "ansible-playbook ansible/docker.yml -i ansible/inventory/host.yml "
                }}}
    
      }
    }
