Follow the tutorials to begin your journey in AI.

# Tutoriel Python : Introduction aux bases
Bienvenue dans ce tutoriel d'introduction à Python. Python est un langage de programmation populaire, connu pour sa simplicité et sa lisibilité. Ce tutoriel vous guidera à travers les bases de Python avec un exemple simple pour vous aider à comprendre les concepts clés.
## 1. Variables en Python
En Python, une variable est simplement un espace mémoire qui stocke une valeur. Vous pouvez créer des variables et les affecter à différentes valeurs.
### Exemple de code :
```python
# Déclaration d'une variable
nom = "Alice"
age = 25
# Affichage des variables
print("Nom :", nom)
print("Âge :", age)
```
Hi, je suis entrain de tester  pour savoir si c'est bon ou pas.

Here is an other test of python code 

```python
# Copyright 2024 X.AI Corp.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

import logging

from model import LanguageModelConfig, TransformerConfig, QuantizedWeight8bit as QW8Bit
from runners import InferenceRunner, ModelRunner, sample_from_model


CKPT_PATH = "./checkpoints/"


def main():
    grok_1_model = LanguageModelConfig(
        vocab_size=128 * 1024,
        pad_token=0,
        eos_token=2,
        sequence_len=8192,
        embedding_init_scale=1.0,
        output_multiplier_scale=0.5773502691896257,
        embedding_multiplier_scale=78.38367176906169,
        model=TransformerConfig(
            emb_size=48 * 128,
            widening_factor=8,
            key_size=128,
            num_q_heads=48,
            num_kv_heads=8,
            num_layers=64,
            attn_output_multiplier=0.08838834764831845,
            shard_activations=True,
            # MoE.
            num_experts=8,
            num_selected_experts=2,
            # Activation sharding.
            data_axis="data",
            model_axis="model",
        ),
    )
    inference_runner = InferenceRunner(
        pad_sizes=(1024,),
       
```
The code above is from grok.
<div class="alert-warning" [href]="trustedUrl">
  <strong>Attention!</strong> This is an important message.
    
 * First item
 * Second item
 * Third item
 * Fourth item
</div>
