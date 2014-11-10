FCM_nips_workshop
=================
Coming soon...

Basic version of FCT model for relation extraction.

Intall:
make

Usage:
./RE_FCT[_fixed] trainfile devfile resfile baseline_embfile num_iter learning_rate

Please use the following command to reproduce the results I reported:
./RE_FCT_fixed data/train.data.se.all.se data/tmpdev.data.se.all.se predict.nodir.i40.5e-2.txt /export/a04/moyu/gigaword_data/models/vectors.nyt2011.cbow.bin 40 0.05

I am sorry that currently early-stopping should be done manually :)

When running on SemEval, it is better to close the sub-models with ne_pair features, 
    since SemEval data uses super sense tags instead of NE tags,
    which have much more number of types and will lead to overfitting.
