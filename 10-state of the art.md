# State of the Art

related work

best work

pros and cons of these systems. constructive

how does it contribute to yours?

**Music gen**

approaches from big paper, in chronological order, from simple to complex, stop at LSTM models. 

mention other model types

**RNNs**

music is sequential - we need to consider previous melodic steps when composing the new one

    The most straight-forward way to compose1 music with an RNN is to use the network as single-step
    predictor. The network learns to predict notes at time t + 1 using notes at time t as inputs. After
    learning has been stopped the network can be seeded with initial input values—perhaps from
    training data–and can then generate novel compositions by using its own outputs to generate
    subsequent inputs. This note-by-note approach was ﬁrst examined by Todd (1989); Bharucha and
    Todd (1989) and later used by others (Stevens and Wiles, 1994; Mozer, 1994).
    A feed-forward network would have no chance of composing music in this fashion. Lacking the
    ability to store any information about the past, **such a network would be unable to keep track of where it is in a song.** In principle an RNN does not suﬀer from this limitation. With recurrent
    connections it can use hidden layer activations as memory and thus is capable of exhibiting (seem-
    ingly arbitrary) temporal dynamics.

what are RNNs

**LSTMs**

problem with RNNs

    RNNs do not perform very well at this
    task. As Mozer (1994) aptly wrote about his attempts to compose music with RNNs, “While the
    local contours made sense, the pieces were not musically coherent, lacking thematic structure and
    having minimal phrase structure and rhythmic organization”.
    The reason for this failure is likely linked to the problem of vanishing gradients(Hochreiter et al.,
    1)    in RNNs. In gradient methods such as Back-Propagation Through Time (BPTT) (Williams
    and Zipser, 1995) and Real-Time Recurrent Learning (RTRL) (Robinson and Fallside, 1987) error
    ﬂow either vanishes quickly or explodes exponentially, making it impossible for the networks to
    deal correctly with long-term dependencies. In the case of music, long-term dependencies are at
    the heart of what deﬁnes a particular style, with events spanning several notes or even many bars
    contributing to the formation of metrical and phrasal structure (Cooper and Meyer, 1960). The clearest example of these dependencies are chord changes. In a musical form like early rock-and-
    roll music for example, the same chord can be held for four bars or more. Even if melodies are
    constrained to contain notes no shorter than an eighth note, a network must regularly and reliably
    bridge time spans of 32 events or more.

LSTM has mechanisms for controlling flow of the backpropagation - the gates

    LSTM is designed to obtain constant error
    ﬂow through time and to protect this error ﬂow from undesired perturbations

**Attention**

in translation, emoji paper

    from https://github.com/CyberZHG/keras-self-attention/blob/master/keras_self_attention/seq_weighted_attention.py

attention allows the LSTM sequence model to learn what steps it should focus on when predicting a new step. In music this intuitively makes sense. We can think of the call-response phrasing, where one initial phrase (the "call") is followed by the same phrase but with a slight change in the ending (the "response"). This is very common in blues rock music.
