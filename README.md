# Machine Translation: RNN, Transformer, and Pretrained Model Implementations
## Overview
This project focused on developing a machine translation system with two main objectives. First, a sequence-to-sequence (Seq2Seq) model was created for translating English to Spanish, utilizing Gated Recurrent Units (GRUs). This was followed by an advanced Seq2Seq Transformer model, both inspired by the work of François Chollet. Additionally, for translating English to Urdu, a pretrained model from Helsinki-NLP was employed to efficiently achieve high-quality results.

The evaluation centered on assessing the latency, complexity, and accuracy of these three approaches to gain insights for educational purposes.

## Implementation Details

#### Seq2Seq with GRU
- Model Architecture: The Seq2Seq model employed GRUs for both the encoder and decoder components. The encoder processes the input English sentences and produces a context vector, which is used by the decoder to generate the Spanish translation.
- Training Process: Used a parallel English-Spanish dataset.
 -Performance: Provided satisfactory translations but struggled with longer and more complex sentence structures.

#### Seq2Seq Transformer
- Model Architecture: Transitioned to a Transformer-based Seq2Seq model to leverage self-attention mechanisms for better handling of dependencies between words.
- Training Process: Continued using the same English-Spanish dataset, incorporating positional encodings and multi-head attention to capture intricate sentence structures.
- Performance: Demonstrated superior translation quality and efficiency compared to the GRU-based model, effectively managing long-range dependencies and improving fluency.

#### Pretrained Model
- Model Choice: For translating English to Urdu, I utilized the pretrained model Helsinki-NLP/opus-mt-en-ur. This model, available from the Hugging Face Model Hub, was specifically designed for English to Urdu translation.
- Implementation: Applied the pretrained model for translation tasks, leveraging its training on a broad range of text to achieve high-quality translations with minimal additional fine-tuning.
- Performance: The pretrained model provided robust translations between English and Urdu, reflecting the effectiveness of leveraging pretrained architectures for specific language pairs.

## Analysis
- Translation Quality: The Transformer model improved translation accuracy and fluency for English to Spanish. The use of Helsinki-NLP/opus-mt-en-ur ensured high-quality translations for English to Urdu with minimal effort.
- Efficiency: The Transformer architecture’s ability to handle long-range dependencies and parallel processing contributed to reduced training times and better performance.
- Pretrained Model Utility: The pretrained model for English to Urdu showcased the practical benefits of using models trained on diverse datasets for rapid deployment in specific translation tasks.

### Model Comparison Table
| Model            | Data Used for Training | Latency           | Implementation Complexity |
|------------------|-------------------------|-------------------|---------------------------|
| RNN              | Yes                     | Slower            | Moderate                  |
| Transformer      | Yes                     | Faster            | High                      |
| Pretrained Model | No                      | Fastest           | Low                       |

## Future Work
- Model Enhancement: Explore advanced Transformer variants or integrate additional contextual information to further enhance translation accuracy and context understanding.
- Multilingual Capabilities: Expand the project to support more language pairs.

## Data Source for English-Spanish Translation Corpus
http://storage.googleapis.com/download.tensorflow.org/data/spa-eng.zip

## Bibliography
François Chollet, “Deep_Learning_with_Python”. Manning Publications. 2021.

## License
This project is licensed under the Raza Mehar License. See the LICENSE.md file for details.

## Contact
For any questions or clarifications, please contact Raza Mehar at [raza.mehar@gmail.com].
