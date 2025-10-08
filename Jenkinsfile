@Library('my-shared-library') _

pipeline {
    agent any

    stages {
        stage('Vars Greeting') {
            steps {
                greet('Alice')
            }
        }

        stage('Class Greeting') {
            steps {
                script {
                    def util = new org.example.GreetingUtils(this)
                    util.greetUser('Alice')
                }
            }
        }
    }
}
