pipeline{
    agent any
    tools{maven 'M3' }
    stages{
        stage('check out'){
            steps{
                git branch: 'main' , url : 'https://github.com/devel-jot/SpringPetClinic'
            }
        }
        stage('build'){
            steps{
                sh 'mvn compile'
            }
            
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('pakage'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /home/coder/.jenkins/workspace/SpringPetClinicDec/target/*.jar '
            }
        }
    }
}
