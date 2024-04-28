@Library("belajar-jenkins-shared-library@main") _

import masterambi.jenkins.Output;

pipeline {
    agent any
    stage("Library Resource") {
            steps {
                script {
                    def config = libraryResource("config/build.json")
                    echo(config)
                }
                
            }
        }
    stages{
        stage("Hello Person") {
            steps {
                script {
                    hello.person([
                        firstName: "Ramzy",
                        lastName: "Rashaun Arief"
                    ])
                }
            }
        }
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