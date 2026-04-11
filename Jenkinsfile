pipeline {
  agent any

  stages {
    stage ('Clone Code') {
      steps {
        git 'Auto trigger test v4'
      }
    }
    stage('Build')
      steps {
        echo 'Building Project....'
        sh 'mkdir build'
        sh 'cp app.txt build/
  }
}
    stage ('Create Artifactory') {
      steps {
        sh 'tar -cvf build.tar build/'
      }
    }
}
post {
  success {
    echo 'Build & Artifact created successfully'
  }
}
}
