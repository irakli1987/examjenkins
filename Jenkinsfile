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
        archiveArtifacts(artifacts: '**.*', fingerprint: true)
        mail(subject: 'test', body: 'test', from: 'jenk', to: 'tkebuchava.irakli@gmail.com')
      }
    }

  }
  parameters {
    choice(choices: ['liverpool', 'liver', 'kolkheti'], name: 'airchie')
  }
}