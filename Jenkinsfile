pipeline {
 agent any
 
 stages {
 stage(‘checkout’) {
 steps {
 git 'https://github.com/kumarinn/jira-jenkins-shared-lib.git'
 
 }
 }

 stage(‘server’) {
 steps {
 dir('/usr/local/bin/terraform/')
 {
 sh '''terraform init
'''
 //sh ‘terraform plan -out=plan’
 // sh ‘terraform destroy -auto-approve’
 //sh ‘terraform apply plan’
 }
 
 
 }
 }
 
 
 
 }
}
