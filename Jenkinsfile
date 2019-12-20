pipeline {

    agent any

    stages {

        stage("Interactive_Input") {
            steps {
                script {

                    // Variables for input
                    def inputConfig
                    def inputTest

                    // Get the input
                    def userInput = input(
                            id: 'userInput', message: 'Enter the Testbed information'\
,
                            parameters: [

                                    string(defaultValue: '130.1.1.1',
                                            description: 'IP Address of Controller',
                                            name: 'IP Address of Controller'),
                                    string(defaultValue: 'TGW:FQDN:CLOUDWAN',
                                            description: 'Tests',
                                            name: 'Tests'),
                                    string(defaultValue: 'Tests for User1....',
                                            description: 'Description of Test Log',
                                            name: 'Description'),
                                    choice(name: 'Tests to Run', choices: "FQDN\nFQDN\
 TWQ\nTGW", description: 'Which Tests to Run?'),
                                    checkbox(name: 'Tests to Run', choices: "FQDN\nTG\
W\nXYZ", description: 'Which Tests to Run?')

                            ])

                    // Save to variables. Default to empty string if not found.
                    inputConfig = userInput.Config?:''
                    inputTest = userInput.Test?:''

                    // Echo to console
                    echo("IQA Sheet Path: ${inputConfig}")
                    echo("Test Info file path: ${inputTest}")

                    // Write to file
                    writeFile file: "inputData.txt", text: "Config=${inputConfig}\r\n\
Test=${inputTest}"

                    // Archive the file (or whatever you want to do with it)
                    archiveArtifacts 'inputData.txt'
                }
            }
        }
    }
}
