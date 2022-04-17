pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        echo "${params.airchie}"
        echo 'Hello World'
        sh 'ls -l'
      }
    }

  }
  parameters {
    choice(choices: ['liverpool', 'liver', 'kolkheti'], name: 'airchie')
  }
}