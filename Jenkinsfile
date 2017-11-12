podTemplate(label: 'sbtPod', containers: [
    containerTemplate(name: 'sbt', image: 'ashee/scala-sbt', ttyEnabled: true, command: 'cat'),
  ]) {

  node('sbtPod') {

      stage('Get sbt project') {
          container('sbt') {
            stage 'checkout'
            checkout scm
            
            stage('Build a sbt project') {
              sh 'sbt dist'
            }
          }
      }
  }
}
