pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Build demo'
        sh '''sh run_biuld_script.sh
'''
      }
    }

    stage('linux test') {
      parallel {
        stage('linux test') {
          steps {
            echo 'hello world'
            sh '''sh run_linux_script.sh
'''
          }
        }

        stage('windows test') {
          steps {
            echo 'hello'
          }
        }

      }
    }

    stage('deploying stage') {
      steps {
        echo 'deploying to prod'
        echo 'wait for interactive input'
      }
    }

    stage('deploy production') {
      steps {
        echo 'to prod'
      }
    }

  }
}