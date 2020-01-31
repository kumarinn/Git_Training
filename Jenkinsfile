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
 env.PATH = “C:\Users\kumarnn\Desktop\Terraform\terraform_0.12.20_windows_amd64\terraform”
 }
 sh ‘terraform — version’
 
 
 }
 }
 
 stage(‘server’) {
 
 steps {
 dir(‘C:\Users\kumarnn\Desktop\Terraform\terraform_0.12.20_windows_amd64’)
 {
 sh ‘terraform init’
 sh ‘terraform plan -out=plan’
 // sh ‘terraform destroy -auto-approve’
 sh ‘terraform apply plan’
 }
 
 
 }
 }
 
 
 
 }
}
