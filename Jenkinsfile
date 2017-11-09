pipeline {
	stage 'checkout'
	checkout scm

	stage 'build'
	sh 'sbt compile'
}