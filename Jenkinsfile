podTemplate(label: 'sbtPod', containers: [
    containerTemplate(name: 'sbt', image: 'hseeberger/scala-sbt', ttyEnabled: true, command: 'cat'),
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
