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
        emailext(attachLog: true, body: 'tuar gezareba xoar wagvevarjisha? ', subject: 'xoar wagvevarjisha', to: 'gio_333m@yahoo.com', from: 'jenkins@globalpharm.ge')
        tool 'irakli'
        junit 'junit.xml'

      }
    }

  }
  parameters {
    choice(choices: ['liverpool', 'liver', 'kolkheti'], name: 'airchie')
  }
}
