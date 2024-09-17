pipeline {
    agent any
    stages {
        stage("setup parameter") {
            steps {
                script {
                    properties([
                        parameters([
                            choice(
                                choices: ["dev", "uat", "prod"],
                                name: "ENVIRONMENT"
                                ),
                            string(
                                defaultValue: "training",
                                name: "STRING")
                            ])
                        ])
                    }
                }
            }
        stage("print parmeter") {
            steps {
                echo "choice parameter is $ENVIRONMENT"
                echo "string parameter is $STRING"
            }
        }
    }
}
