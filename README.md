# Topic: Ancient Sci-fi
- This project is a machine-generated sci-fi novel using GPT-2. The story is an alien-invasion story. Facing this huge trouble, people turn to the ancient militarists for help. The story displays a discussion/debate between Sun Tzu and Napoleon.
# Conceptual background
- The idea comes from a popular Chinese Science fictional novel <The Three Body Problem> written by Liu Cixin. This novel is about a story that aliens are going to invade earth. There is one virtual reality game in this story which is installed with modelled characters of ancient scientists, philosophers and emperors —— Darwin and the Chinese Emperor Zhou You Wang. Their minds are simulated and put into those VR characters so that the players can have a conversation with those ancient people.
- Inspired by this game, I decide to also tell a story of alien invasion, and "invites" some intelligent militarists to discuss on this issue. I choose two representative militarists from both the East and the West. The first militarist is Napoleon, the second is one of the most famous Chinese militarists called Sun Tzu. I think they can develop an interesting conversation, or debate on the futuristic topic about how to treat aliens.
# How the Algorithm works
- For the three paragraphs, I create 3 models for GPT2 generating. For the first model, I upload the whole text of the book <The Dark Forest>, which is the second book of the Three Body Problem series, and let GPT-2 get trained. For the second model, I upload the book <The Art of War> written by Sun Tzu. I replace words like "enemy" and "opponents" with "aliens" to make the file to be trained more sci-fi like. For the last model, I scrape down some quotes of Napoleon from a website. I also replace the words just as what I did for Sun Tzu. 
- I structure the storyline like this: (1) I begin the story with a line "The alien is coming to earth", and let gpt2 generate the first paragraph with the model of Three Body. (2) I begin the second paragraph with the line "To face this new strange guest, people turn to the oldest and the brightest minds for help. \nThe Official:"Masters, how should we fight with the alien?", then the code will generate a saying of Sun Tzu. After that, the code will using the Sun Tzu's saying as prompt to generate Napoleon's sayings. Thus, a discussion is formed through this kind of repetitive generation. (3) Finally, the code will generate an ending using the previous paragraphs as a prompt and a beginning sentence "the alien finally comes" using the Three Body model to talk about what happens when the alien finally arrives.
# Exploring Topics and Difficulties
- I am exloring how to simulate the speaking of people and create dialogues using GPT2. The solution I find is to create saparate models. As the GPT2 code is kind of new and challenging to me, I find it difficult to assign the models into three and assign them to each paragraph. Therefore, I just run the model before it is needed. When I need to generate Sun Tze, I click Load Checkpoint for Sun Tzu model, and I load the Napoleon when I need to generate. To make the process clearer and simpler is what I am going to do in the future. 
- My initial idea is to make two situations. One is when people regard aliens as evil (I may let the reader input an adjective describing the alien and use TextBlob to anaylze the sentiment). And the militarist will discuss about war. And the other is when people regard aliens as great and intelligent, then some philosophers like Confucius will discuss about how to treat them as friends. I want to explore more possibilities on this story.
# How the Presentation Shapes the Readers' Response
- The reason why I choose this kind of interactive webpage is that I wish to make the readers believe they are engaging this serious discussion a part of the human beings although now the readers actually do not have the right to change the plot. But in the future, I may list some optional answers by Napoleon after listening to Sun Tzu's words, and the dialogue can go with the reader's decisions, which make the storytelling more flexible and create more engagement and interactions. 
