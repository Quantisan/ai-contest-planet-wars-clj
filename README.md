## How to use this bot:

To work with the default bot.clj, ensure you have [leiningen](github.com/technomancy/leiningen) up and working and do the following:

    $ lein uberjar
    > ... 
    > clpw-pwars-1.0.0-SNAPSHOT-standalone.jar 
    
    $ mv clj-pwars-1.0.0-SNAPSHOT-standalone.jar clpw.jar
    
    $ java -jar tools/PlayGame.jar maps/map7.txt 3000 1000 log.txt "java -jar example_bots/RandomBot.jar" "java -hotspot -jar clpw.jar" | java -jar tools/ShowGame.jar

And you should be good to go.

## Notes

Note that the start-up time is 3000ms instead of 1000; this is because it takes about that long for the JVM to get going with Clojure. 

Hopefully there will be an update to the game engine that doesn't penalize slow start-up times (e.g. both bots send "OKAY" when they're all ready, *then* recieve the map/game-state from the game engine.)

The contest is hosted at [ai-content.com](ai-contest.com)

* * *

Please report any errors or bugs at http://github.com/ihodes/ai-contest-planet-wars-clj