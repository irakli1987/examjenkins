pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        stash 'files'
        sh 'rm README.md'
        echo "${params.airchie}"
        echo 'Hello World'
        sh 'ls -l'
      }
    }

    stage('naxvamdis') {
      steps {
        unstash 'files'
        echo "${params.airchie}"
        echo 'Hello World'
        sh 'ls -l'
        archiveArtifacts artifacts: '**.*', fingerprint: true, followSymlinks: false
      }
    }

  }
  parameters {
    choice(choices: ['liverpool', 'liver', 'kolkheti'], name: 'airchie')
  }
}
