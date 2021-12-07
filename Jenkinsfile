node{
    stage("Fetch Source Code"){
        git 'https://github.com/skyhitnow/Beginning-Jenkins'
    }


dir('Lesson5'){
    printMessage('Running Pipeline')
    
    stage("Testing"){
        sh 'python test_functions.py'
    }
    
    stage("Deployment"){
        if(env.BRANCH_NAME=='master'){
            printMessage('Deploying the master branch')
        }else{
            printMessage('No deployment configured for this branch')
        }
    }
    printMessage('Pipleline Complete')
}

}

def printMessage(message){
    echo "$message"
}



