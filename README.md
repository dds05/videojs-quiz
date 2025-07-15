# videojs-quiz
Interactive quiz for video.js player.<br/> <br/>
This plugin brings interactive quizzes to videos, allowing users to answer multiple-choice questions directly within the player.<br/>
It ensures active participation by requiring users to complete the quiz before continuing playback, making it ideal for e-learning, training, and interactive engagement.

## Installation
`npm i videojs-quiz`


## Getting Started

Post installation, import and use the package like shown below:-
```
import 'videojs-quiz';

var quizData = [
  {
    questionId: '1',
    time: 5, // Time (in seconds) to pause for the quiz
    question: 'What is the capital of France?',
    answers: ['Berlin', 'Madrid', 'Paris'],
    correctAnswer: 2, // Index of the correct answer
  },
  {
    questionId: '2',
    time: 10,
    question: 'Which planet is known as the Red Planet?',
    answers: ['Earth', 'Mars', 'Jupiter', 'Venus'],
    correctAnswer: 1,
  }
]; 
   
 const player = videojs(playerId,options);  //initialise videojs player

  player.on('ready', () => {
      // initialise quiz data
      player.quiz({
        quizData: quizData
      });

      // listener for answer selection
      player.on('quizAnswer', (e) => {
        console.log('Selection: ', e.detail);
      })
  })

 
```



