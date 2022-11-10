pipeline {
  agent any
  stages {
    stage('pull') {
      steps {
        script {
          checkout([$class: 'GitSCM', branches: [[name: '*/'main']],
                  userRemoteConfigs: [[
                      credentialsId: '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',
                      url: 'https://github.com/AlaaEddineBoukhriss/AngApp.git'
                    ]
                  ]
                ])
            }
          }
        }
      }
    }
