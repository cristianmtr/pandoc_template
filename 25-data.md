# Dataset

**Description**

folk dataset 

is a collection of traditional Irish tunes from https://thesession.org/

Where did you get the data from

prepared by https://github.com/IraKorshunova/folk-rnn

hooktheory

scraped from net using https://github.com/cristianmtr/Lead-Sheet-Analysis

**Stats**

nr tunes

average length
std length

keys

use mgeval and jsymbolic

**encoding process**

4/4

transpose to CMajor / A Minor

monophonize

score format

1. score encoding is more efficient, ~25 steps per bar, vs 96 for pianoroll
1. less sparse

final nr of sequences for each dataset