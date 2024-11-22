# Mg<sub>2</sub>GeSe<sub>4</sub> MLIP

Supporting information for: ["Effects of Four-Phonon Scattering and Wave-like Phonon Tunneling Effects on Thermoelectric Properties of Mg2GeSe4 using Machine Learning"](https://arxiv.org/abs/2411.10605), Hao-Jen You, Yi-Ting Chiang, Arun Bansil, Hsin Lin. (Preparation)

## MLIP type: MACE
MACE version: v0.3.6

Training details:
```
--name="MACE_model" \
--train_file="./training_data/train.xyz" \
--valid_fraction=0.05 \
--test_file="./training_data/test.xyz" \
--config_type_weights='{"Default":1.0}' \
--E0s='average' \
--model="MACE" \
--num_interactions=2 \
--num_channels=16 \
--max_L=2 \
--r_max=9.0 \
--batch_size=10 \
--max_num_epochs=500 \
--swa \
--start_swa=400 \
--ema \
--ema_decay=0.99 \
--amsgrad \
--restart_latest \
--default_dtype="float64"\
--device=cuda \
--distributed \
--save_cpu \
```

## Reference:
[1]: [MACE - Fast and accurate machine learning interatomic potentials with higher order equivariant message passing](https://github.com/ACEsuit/mace)
