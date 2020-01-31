@Library('jira-jenkins-shared-lib') _
pipeline
agent any
environment {
JIRA_BASE_URL=
JIRA_CREDENTIALS_ID=
SLEEP_TIME=
APW_APPLICATION=
APW_UNAVAILABLE_STATUS=
APW_AVAILABLE_STATUS=
VERSION=readMAVENPOM().getVersion()
}
parameters {
choice(name:'Choices of Environments',choices:['Dev','Test'],description:'Do you want to deploy ?')
}
tools {
maven 
jdk
}
stages {
stage('BUILD ABD TEST') {
steps {
bat 'mvn clean install'
}
}
stage('Deploy on Dev') {
when {
equals expected:'Dev',actual:params.Choices of Environments
}
environment {
