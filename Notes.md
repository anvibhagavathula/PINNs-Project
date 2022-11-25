## Notes:

# 24/11/22 - Load and Save Models

    - Need to find way to load and save models for Jax, current models take ~12min to train. 
    Potential solution: https://github.com/google/flax/discussions/1876 Would need to be able to 
    toggle between retraining and loading at will. Considering we aren't using flax, we might
    want to save /load models via pickle instead: 
    https://stackoverflow.com/questions/64550792/how-do-i-save-an-optimizer-state-of-jax-trained-model
    Jax doesn't have native support for loading and saving models, so we will need to either use
    other libraries or we could save the weights and biases in a list format and then write a script 
    in which we initialize the model with the saved weights and biases.  
    Fix: See runner.py for more information.
            Notes: 
            - Will need to separate the model builder from the visualiser in this doc.
            - Will try and immitate the code from HW5 -> toggle between retraining and loading in
            the terminal.
            - Need to restructure code into classes to allow this. Current code slightly unreadable.
            - Incomplete burgers_model.py revamp.
            - runner.py hasn't been started.

# 25/11/22

    - burgers_preprocessing.py complete, need to integrate into runner.py
    - visualiser.py structurally complete still needs to be debugged (see Debugging.md). Need to 
    integrate into runner.py
    