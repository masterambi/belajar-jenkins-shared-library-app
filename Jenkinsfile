@Library("belajar-jenkins-shared-library@main") _

import masterambi.jenkins.Output;

pipeline {
    agent any
    stages{
        stage("Global Variable") {
            steps {
                echo(author.name())
                echo(author.channel())
            }
        }
        stage("Hello Groovy") {
            steps {
                script {
                    Output.hello(this, "Groovy")
                }
            }
        }
        stage("Hello World") {
            steps {
                script {
                    hello.world()
                }
            }
        }
    }
}