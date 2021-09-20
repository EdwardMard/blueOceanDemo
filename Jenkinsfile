pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/EdwardMard/newvagrantfile.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'This is build ;)'
      }
    }

    stage('Deploy to Dev1') {
      parallel {
        stage('Deploy to Dev1') {
          steps {
            sleep 30
            echo 'finished'
          }
        }

        stage('Deploy to Dev2') {
          steps {
            sleep 40
            echo 'completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing...'
      }
    }

  }
}