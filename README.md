# EmotionalConversationAgent

## Prerequisites

    1) Create a conda virtual environment named KerasTheano
        i) Install keras version 1.1.0
        ii) Install theano version 0.8.2
    2) Create a conda virtual environment named Scikit0.20.1
        i) Install scikit-learn version 0.20.1
        ii) Install numpy version 1.14.6
    3) Create a conda virtual environment named Keras2.2.4
        i) Install keras version 2.2.4
        ii) Install tensorflow version 1.10.0
    4) Installations for Web server
        i) Install npm : https://www.npmjs.com/get-npm 
        $ cd stats_webpage
        $ npm install -g nodemon
        $ npm install --save express socket.io
    5) Python socket-io client
        $ git clone https://github.com/nexus-devs/socketIO-client-2.0.3
        $ cd socketIO-client-2.0.3
        $ python setup.py install
       
       
## Running


    1) In a terminal, run the classifier to predict emotion of sentence
        $ source activate KerasTheano
        $ python socket_classify.py
    2) In a different terminal, run the classifier to predict response emotion
        $ source activate Scikit0.20.1
        $ python  socket_pickdecoder_classifier.py
    3) In a different terminal, run the reply generating model
        $ source activate Keras2.2.4
        $ python socket_6decoderreply.py
    4) In a different terminal, set up the webserver
        $ cd stats_webpage
        $ nodemon server.js
    5) Once all the sockets are set up and the output shows them listening at the specific ports, run the telegram bot
        $ python telegram_emotion_bot.py
    6) Converse with the bot, and go to localhost:300/pie , localhost:300/line and localhost:300/graph to see various graphs for the cnversation
