podTemplate(label: 'sbtPod', containers: [
    containerTemplate(name: 'sbt', image: 'pplenik/jnlp-slave-sbt-build-tools', ttyEnabled: true, command: 'cat'),
  ]) {

  node('sbtPod') {

      stage('Get sbt project') {
          container('sbt') {
              stage('Build a sbt project') {
                sh 'sbt dist'
              }
          }
      }
  }
}
