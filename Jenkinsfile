pipeline {
 agent any
 
 stages {
 stage(‘checkout’) {
 steps {
 git 'https://github.com/kumarinn/jira-jenkins-shared-lib.git'
 
 }
 }
 stage(‘path’) {
 steps {
 script {
 env.PATH = “/usr/local/bin/terraform”
 }
 sh ‘terraform — version’
 
 
 }
 }
 
 stage(‘server’) {
 
 steps {
 dir(‘/usr/local/bin/terraform/ec2-ubuntu.tf’)
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
