pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            
            steps {
                bat 'C:\\Users\\spencer\\Documents\\Nuget\\nuget.exe restore %WORKSPACE\\ConsoleApp\\ConsoleApp.sln'
                bat '"C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\Community\\MSBuild\\Current\\Bin\\MSBuild.exe" %WORKSPACE%\\ConsoleApp\\ConsoleApp.sln'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}