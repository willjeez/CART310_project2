Will Graham-Simpkins
CART310
Translational Reality Project

I became interested in coding because I am interested in game design. I am particularly interested in designing a game's "feel", so I knew for this project I wanted to make a "one-button game". I had been learning Processing and then Javascript, so I wanted to expand upon a clicker game I was making to learn Jquery.

Originally, the game was simply clicking a button to increase a number. There was no audiovisual aspect, no real rules, and no established "feel". I wanted to use the Translational Reality project to expand on what I had and make a game of sorts that could also function as an installation.

First, I had to decide what the button did. Since the idea was based on the myth of Sisyphus - whose punishment was chosen to be to push a rock up a hill for eternity, only to have it roll back down once he reached the top - it made sense to have pressing the button push the rock a certain distance. Obviously, however, it needed more complexity in order to generate a "feel". I wanted to translate what the struggle must have felt like.

Three key elements were incorporated to facilitate the generation of struggle:
1. Sisyphus must "power up" before pushing the rock.
2. Sisyphus becomes more fatigued with each action.
2. The rock will periodically slip, based on the amount of fatigue.

Thus the fundamental "game" aspect was established as the interplay between these three elements that form the foundation behind the action of pushing the rock. Details as to how the values interact with each other are described in the js/script.js comments.

Sound was added to support the feeling of progress. The hill is split into 6 sections, and each section corresponds to a note in a chord. The amplitude of each note is individually raised as Sisyphus pushes the rock up through each section. The music is based off the intro music from the Super Nintendo game Final Fantasy VI, which is also from where I ripped the sample of the organ note. The visual aspect (made using p5) was added afterwards, and was kept simple. A text log is generated documenting the effect of the player's actions.

Since the player has two actions they can make (push the rock or power up), I had those actions mapped to pressing the button repeatedly and holding the button down, respectively. The amount of button presses required is meant to have your arm get at least a little bit tired, simulating Sisyphus's struggle. The game aspect comes from balancing when to push, when to power up, and when to let off the button to restore some of your fatigue. This simple interplay, after hours of balancing the values, turned out to be surprisingly fun in practice.

The game also keeps track of and displays how many times the summit has been reached, which works in an installation context: players would see the game and experiment with the button, and maybe think it's too hard - but they would see that the summit had in fact been reached before, prompting them to change their strategy and push themselves to "solve" the game. I watched this happen in real time when I had others test it and it was interesting to see the different approaches/reactions.

It was fun to have others test the game, as I would show it to them without explaining how to play/what to do. The lack of explanation or "how to play" facilitates experimentation. Some caught on quickly and others took a little more time. Watching the different approaches different players took in regards to powering up/pushing the rock, and watching their frustration as their fatigue levels prevented them from making meaningful progress made me feel successful in what I was trying to accomplish: something that seems extremely basic at the outset, but which generates a "feel" as soon as one begins to play.

I used a tea box as the enclosure for the arcade button, painted it, and wired the button to the Circuit Playground Express as a keyboard controller using copper wire and alligator clips. Pressing the button is identical to pressing the 'a' key on your keyboard. I ran into issues with the CPE code when it came to the holding aspect, but those were solved when I generated the code using Makecode (circuitplayground-arcade button a4.uf2). The script interprets pressing the button as one action, and holding it as another, and runs the respective code depending on user input. Regrettably, the Makecode version seems to have trouble processing extremely fast button presses, negatively affecting the desired "feel".

As mentioned, the button is simply an auxiliary 'a' key, thus the game is playable without external hardware by simply pressing & holding 'a' on your keyboard.
