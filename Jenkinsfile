pipeline{
 agent any 
stages{
 stage('#1.chechout'){
  steps{
    git url:'https://github.com/Maheshkumarthevar/Docker-B2',branch:'main'
}
}
stage('#2. Build the image'){
  steps{
   bat 'docker build -t mywebsite .'
     }
   }
     stage('#3. Stop all old containers'){
steps{
bat'docker stop mycont || exit 0'
bat 'docker stop mucont || exit 0'
  }
}

stage ('#4. Run the image - containerise'){
 steps{
bat 'docker run -d -p 4000 -- name mycount mywebsite'
}
}

}
}
