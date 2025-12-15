
## machine learning

A machine learning algorithm uses an initial data set to build an internal model which it uses to make predictions. It tests these predictions against additional data and uses the results to refine the model.

90% of all the data in existence was created in the last two years.

Turning Big Data into information and thence into understanding and insight is the job of algorithms.

Having more data beats having better data if what you want is to be able to understand, predict and influence the behaviour of large numbers of people.

Traditionally, statisticians started with a hypothesis and went to look for data to support or refute it.
Machine learning, by contrast, starts with data - lots of it - and looks for patterns.

Supermarkets use algorithms to predict what we will collectively want to buy, when and where.
Hospitals use AI to allocate beds.
Telecoms companies, power generators and other utilities use it to manage the load on their resources.

## neural networks

An artificial neural network represents the state of each neuron by a single number and the strength of each synapse by a single number.
In this model, each neuron updates its state at regular time steps by simply averaging together the inputs from all connected neurons, weighting them by the synaptic strengths, optionally adding a constant, and then applying what's called an activation function to the result to compute its next state.
The easiest way to use a neural network as a function is to make it feedforward, with information flowing only in one direction, plugging the input to the function into a layer of neurons at the top and extracting the output from a layer of neurons at the bottom.

Backpropagation retraces the steps in a neural net to identify the errors made in an initial processing of input data.

Convolutional networks: the neurons in each layer are only connected to groups of neurons in the next layer.
Recurrent networks: connections from each layer can loop back to an earlier layer.

## reinforcement learning

Basic reinforcement learning is a classic machine learning technique inspired by behaviorist psychology, where getting a positive reward increases your tendency to do something again and vice versa.
DeepMind combined this idea with deep learning: they trained a deep neural net to predict how many points would on average be gained by pressing each of the allowed keys on the keyboard, and then the AI selected whatever key the neural net rated as most promising.
That's deep reinforcement learning.

If you're a robot, life itself can be viewed as a game.
All that's needed is a system that gives it points whenever it makes progress.

AlphaGo displayed both intuition and creativity.
Combining the intuition of deep learning with the logic of "good old-fashioned AI" can produce second-to-none strategy.
AlphaGo was to marry the intuitive power of deep learning with the logical power of "good old-fashioned AI".
They used a massive database of Go positions from both human play and games where AlphaGo had played a clone of itself, and trained a deep neural network to predict from each position the probability that white would ultimately win.
They also trained a separate network to predict likely next moves.
They then combined these networks with a "good old-fashioned AI" method that cleverly searched through a pruned list of likely future-move sequences to identify the next move that would lead to the strongest position down the road.

The Winograd Schema Challenge asks what "they" refers to here:
1. "The city councilmen refused the demonstrators a permit because they feared violence."
2. "The city councilmen refused the demonstrators a permit because they advocated violence."

It's getting progressively harder to argue that AI completely lacks goals, breadth, intuition, creativity or language.

Verification asks "Did I build the system right?"
Validation asks "Did I build the right system?"

Does the system rely on assumptions that might not always be valid?
If so, how can it be improved to better handle uncertainty?

## what ml is - to ben bryan 2024-07

D. AI - You're very, very correct about machine learning becoming a vastly powerful tool. I remember hearing in my accounting discipline that the 1980s had people speculating that the spreadsheet would replace the accountant. It certainly did: on the most boring parts of the job! But, it didn't replace two complexities: interpreting complicated legal code and finding out how to legally prevent the government from taking as much money as possible (tax), and skimming through a paper trail of documents to make sure there was sufficient evidence that things were recorded properly (audit).

Machine learning itself is simple: it's an algorithm that makes its own rules. So, you can pass through 10,000 photos of pens, or 8,000 movie scripts, or 65,000 photos of smiling people, and it'll form common logical elements that hold the whole thing together.

The downside, though, is that ML is also still a dumb computer. I remember an anecdote where visible skin diseases weren't getting diagnosed correctly, until they found out the algo correlated that you had a skin disease if you had a ruler next to your arm. The training data picked up that secondary thing that human perception would logically rule out.

This alludes to a point that I'm frustrated can't be sequentially expressed (but I'm emailing you instead of writing an essay so I'll stop kicking myself and get to the point). Machine learning is a logic-based computer that has been programmed to create a type of "intuition". Human perception, by contrast, is the primitives of our brain stem's emotions, configured to create a type of "logic/reasoning" sitting on top of it. However, I know you've read enough philosophy to know that a logically true statement will be easily interfered with by common sense (All Cars are Hats, so some Hats are Cars, right?).

The reason this won't float in the tech community, at least until they throw a few more billion on top of the 60+ billion sunk cost they've assembled, is due to their defective philosophy of humanity. Secular humanism (especially among the tech world) usually consists of naturalists, with the most dramatic version of the idea being that "soul", "brain", "mind", and "psyche" are all semantically the same thing. To the believer in any form of God (and, more particularly, the existence of humanity beyond bodily existence), that's absurd.

The irony is that we have logical evidence of there being something else: Mary Shelley's Frankenstein was a conjectural reality of the time, and there is certainly a thing that exists in a living being that certainly disappears after a primary organ fails, never to return to that being, even within a few short minutes of ceased existence.

But, if there is nothing but biomechanics, the modern tech person falls into the same trap as the 19-century scientist or Progressive of the time. This time, though, it's not a mechanical object, but a computer.

And, therefore, we have a machine learning algorithm, which has many effective uses, but will be hyped into something it really isn't. Our myth-making tendencies aren't without irony, either: they're consulting the bullshit generator as if it were a soothsayer of its own. It'd be more accurate if they took away hallucination (where it just makes up stuff when it doesn't know), but that would also make it spit out more errors and throw out the suspension of disbelief among users.

The spirit of this machine learning works antithetically to anyone conditioned to using a computer. When veteran tech people turn on the computer, they expect precise answers when they enter "netstat" or "sudo install vlc", with the computer saying "durr dunno error" if it's not precise. We don't want it to make up stuff when it doesn't know. If this hype train doesn't slow soon, I see a catastrophic failure of an OS coming.

The margin of error on these ML models never seems to get below ~20%. I'm convinced it's because the implementation of absolutely everything in life itself is far too complex to be fully understood. I believe God designed reality that way to keep us humble through trusting others.

So, the best thing is to invest in AI on the boring-as-bricks stuff that must be done the same way a bazillion times (e.g., factory machinery, quality control) and treat the rest as a dying trend that's a magnification of the "no worries put it in the cloud!" dialogue of our past. 
