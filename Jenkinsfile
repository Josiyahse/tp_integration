pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk '11.0.13'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'printenv'
                withMaven(mavenSettingsConfig: 'maven-settings-global') {
                    sh 'mvn clean package'
            }
        }
    }
}
}
// Script //
node {
    stage('Initialize') {
        echo 'Building....'
    }
    stage('Build') {
        bat "set"
            withMaven {
                git changelog: false, poll: false, url: 'https://github.com/Josiyahse/tp_integration.git'
        
                bat "mvn package"
            }
    }
}