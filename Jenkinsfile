pipline{
    agent{label 'master'}
    tools{maven 'M3'}https://github.com/hari10105/SpringPetClinic.git
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/hari10105/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
        }
    }
    stage('Test'){
        steps{
            sh 'mvn test'
        }
    }
    stage('package'){
        steps
        sh 'mvn package'
    }
}
stage('Depoly'){
    steps{/
        sh 'java -jar /var/lib/jenkins/workspace/PetclinicDeclarativePipeline/target/.jar'
    }
}
