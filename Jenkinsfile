@Library("belajar-jenkins-shared-library@main") _

import masterambi.jenkins.Output;

pipeline {
    agent any
    stage("Hello Person") {
            steps {
                script {
                    person.person([
                        firstName: "Ramzy",
                        lastName: "Rashaun Arief"
                    ])
                }
            }
        }
    stages{
        stage("Maven Build") {
            steps {
                script {
                    maven(["clean", "compile", "test"])
                }
                
            }
        }
        stage("Global Variable") {
            steps {
                echo(author())
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