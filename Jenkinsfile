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
