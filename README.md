# public
https://ashuang2013.github.io/public/. 

public/7-7Response
# QUESTION 1
'''
According to Maroney, Machine Learning is using the computer to create the rules that governs a program using both input and output data. The difference
between traditional programming and machine learning is the orientation of the process of writing code. For traditional programming, the programmer looks
at the input and output and formulates rules that govern them and the write the code. For machine learning, instead of the programmer writing the rules, 
the machine will look at both the input and the output and find the rules that govern them.
'''

# QUESTION 2
model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])
xs = np.array([-1.0, 0.0, 1.0, 2.0, 3.0, 4.0], dtype=float)
ys = np.array([-2.0, 1.0, 4.0, 7.0, 10.0, 13.0], dtype=float)
model.compile(optimizer='sgd', loss='mean_squared_error')
print(model.predict([7.0]))

# The first prediction is 21.996738
# The second prediction is 21.999975

# QUESTION 3
import tensorflow as tf
import numpy as np
from tensorflow import keras
model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])
model.compile(optimizer='sgd', loss='mean_squared_error')
newx = np.array([4.0, 3.0, 5.0, 4.0, 2.0, 3.0], dtype=float)
newy = np.array([399.0, 97.0, 577.2, 289.0, 250.0, 229.0], dtype=float)
model.fit(newx, newy, epochs=500)
b2 = model.predict([2.0])
b3 = model.predict([3.0])
b4 = model.predict([4.0])
b5 = model.predict([5.0]) 

h1 = 399-b4
h2 = 97-b3
h3 = 577.2-b5
h4 = 289-b4
h5 = 250-b2
h6 = 229-b3

print('4 Bedroom ' + str(h1))
print('3 Bedroom ' + str(h2))
print('5 Bedroom ' + str(h3))
print('4 Bedroom ' + str(h4))
print('2 Bedroom ' + str(h5))
print('3 Bedroom ' + str(h6))

'''
The home that costs $97,000 with 3 bd and 1 ba is the best deal since it has the greatest difference from the predicted price using the model that was fit to the 6 homes.
The home that costs $577,200 with 5 bd and 2 ba is the worst deal since it has the greatest difference from the predicted price using the model.
'''

    © 2020 GitHub, Inc.
    Terms
    Privacy
    Security
    Status
    Help

    Contact GitHub
    Pricing
    API
    Training
    Blog
    About

