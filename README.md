# Prompt Engineering — Comparing Generative AI Models on Identical Prompts

**Register No:** 212223220009

## Objective

Compare the behaviour of different Generative AI models using identical prompts, evaluating each on **Accuracy**, **Creativity**, **Hallucination**, **Reasoning**, **Speed**, and **Engineering usefulness** for the topic of Generative AI and Large Language Models (LLMs).

## Experiment

Develop a comprehensive report for the following exercises:

1. Explain the foundational concepts of Generative AI.
2. Focusing on Generative AI architectures (like transformers).
3. Generative AI architecture and its applications.
4. Generative AI impact of scaling in LLMs.
5. Explain about LLM and how it is built.

Tools compared: **[Tool 1 — e.g.CLAUDE ]** and **[Tool 2 — e.g. ChatGPT]**

---

## Prompts Used

### Prompt 1 — Foundational Concepts
> Explain the foundational concepts of Generative AI for a college-level audience. Cover its definition, historical background, the difference between discriminative and generative models, and why deep learning enabled its rise. Use simple language with real-world analogies.

### Prompt 2 — Architectures (Transformers)
> Explain the architecture of Generative AI models, focusing on Transformers. Compare Transformers with GANs and VAEs, and describe how self-attention allows Transformers to process data more efficiently. Include a simple example illustrating how a Transformer processes a sentence.

### Prompt 3 — Architecture and Applications
> Describe how Generative AI architecture translates into real-world applications. Explain at least 5 applications across categories like image generation, video generation, audio/speech, code generation, and conversational AI, linking each application to the underlying architecture (GAN, VAE, or Transformer) that powers it.

### Prompt 4 — Impact of Scaling in LLMs
> Explain the impact of scaling on Large Language Models (LLMs). Discuss how increasing model size, training data volume, and compute resources affects performance, and describe the challenges involved (e.g., overfitting, cost, distributed training). Use current examples like GPT-3 vs GPT-4.

### Prompt 5 — How LLMs Are Built
> Explain what a Large Language Model (LLM) is and describe step-by-step how it is built — from data collection and tokenization, through pre-training, to fine-tuning and RLHF. Explain the role of the Transformer architecture and self-attention in this process.

---



### Tool 1: Claude

**Prompt 1 Response:**
```
Generative AI (GenAI) is a branch of artificial intelligence focused on creating new content — text,
images, audio, video, or code — rather than simply analyzing or classifying existing data.

Historical background: Neural networks date back to the 1950s (the perceptron), but were limited to
a handful of layers until the 1990s. The 2010s brought "deep learning" — networks with many stacked
layers — which unlocked a key property: unlike traditional machine learning, whose performance
plateaus as more data is added, deep neural networks keep improving as they're fed more data and
compute. This scalability is what allowed modern GenAI to emerge.

Discriminative vs. generative models: Discriminative models make a decision about input data — e.g.,
classifying an email as spam or not. Generative models instead learn the underlying patterns of data
well enough to produce new, similar data — e.g., writing a new email in a given style.

Analogy: think of a discriminative model as an art critic who can tell a real Picasso from a fake, and
a generative model as an apprentice who has studied Picasso's work so thoroughly they can paint an
original piece in his style.

Foundation models: GenAI systems are often built as "foundation models" — trained on massive, diverse
datasets so they can be adapted to many downstream tasks without needing to be built from scratch
each time.
```

**Prompt 2 Response:**
```
Three main architectures power modern Generative AI:

1. GANs (Generative Adversarial Networks) — Two networks compete: a Generator creates fake data, and
   a Discriminator tries to tell real from fake. As they compete, the Generator gets better at
   producing convincing output. Analogy: a forger and an art detective locked in an escalating duel —
   the forger's fakes get better as the detective gets sharper at spotting them.

2. VAEs (Variational Autoencoders) — An Encoder compresses input into a compact "latent" representation,
   and a Decoder reconstructs it, allowing controlled variation. Useful for generating smooth variations
   of existing data (e.g., new faces that blend features of training faces).

3. Transformers — Unlike GANs/VAEs, Transformers process an entire sequence at once rather than
   step-by-step, using a mechanism called self-attention to weigh how much each word/token should
   "pay attention to" every other token in the sequence. This lets them capture long-range context
   efficiently and in parallel — making them far more GPU-friendly than older sequence models (like
   RNNs) that had to process tokens one at a time.

Example: In the sentence "The trophy didn't fit in the suitcase because it was too big," self-attention
lets the model figure out that "it" refers to "the trophy," not "the suitcase," by weighing the
relationships between all the words simultaneously rather than reading left-to-right in isolation.

Transformers underlie nearly all modern large-scale GenAI systems, including GPT and BERT.
```

**Prompt 3 Response:**
```
Generative AI architectures map onto real-world applications as follows:

1. Image generation (GANs / Diffusion models) — Text-to-image tools generate realistic images from
   text descriptions, used in design, advertising, and media.

2. Video generation & prediction (GAN/Transformer hybrids) — Models generate new video frames or
   predict future frames from existing footage; used in content creation and in anomaly detection
   for security/surveillance.

3. Audio & speech (GANs) — Text-to-speech systems produce natural-sounding voice audio, used to
   convert books into audiobooks and to power voice assistants.

4. Code generation (Transformers) — Large language models trained on code repositories can write,
   complete, or debug code, lowering the barrier to software development for both engineers and
   non-programmers.

5. Conversational AI (Transformers) — Chatbots and virtual assistants use Transformer-based LLMs to
   generate natural-language responses, powering customer support, tutoring, and assistant apps.

6. Semantic image-to-photo translation (GANs) — Converting sketches or semantic maps into realistic
   images, useful in healthcare imaging and design prototyping.

Each application relies on the same core idea — learning a data distribution well enough to sample
new, realistic examples from it — but the specific architecture chosen depends on the data type
(sequential text favors Transformers; pixel-grid data has historically favored GANs and diffusion
models).
```

**Prompt 4 Response:**
```
Scaling refers to increasing an LLM's size, training data, and compute resources — and it has a
disproportionately large effect on capability, often producing qualitative jumps in performance
rather than just incremental gains (sometimes called "emergent abilities").

1. Model size — More layers and parameters increase the model's capacity to represent complex
   patterns, but raise training time, cost, and overfitting risk if data doesn't scale proportionally.

2. Training data volume — Larger, more diverse datasets improve generalization and reduce overfitting,
   but collecting, cleaning, and de-biasing data at scale is expensive and technically challenging.

3. Compute resources — More GPUs/TPUs enable faster, more thorough training and experimentation, but
   at rising financial and environmental cost, and with resource access itself becoming a competitive
   advantage (favoring large, well-funded labs).

4. Distributed training — Splitting training across many machines is necessary at scale, but
   introduces communication overhead and synchronization complexity requiring specialized engineering.

Example: The jump from GPT-3 to GPT-4 illustrates this — increases in scale and training
sophistication correlated with substantial gains in reasoning, instruction-following, and reduced
(though not eliminated) hallucination, even though the underlying Transformer architecture stayed
conceptually similar.
```

**Prompt 5 Response:**
```
A Large Language Model (LLM) is an AI system trained to understand and generate human language by
predicting the most likely next token (word or sub-word unit) given the tokens before it — rather
than retrieving facts from a fixed database.

Build process:
1. Data collection — Massive text corpora are gathered from books, websites, articles, and code
   repositories.
2. Preprocessing — Text is cleaned and split into tokens; tokens are converted into numerical vectors
   called embeddings that capture semantic meaning.
3. Pre-training — Using the Transformer architecture, the model repeatedly predicts the next token in
   a sequence, adjusting its internal parameters based on how wrong its predictions were. Self-attention
   lets it weigh which earlier words matter most for predicting the next one. This is the most
   computationally expensive stage, often requiring thousands of GPUs over weeks or months.
4. Fine-tuning — The pre-trained model is further trained on smaller, task-specific datasets (e.g.,
   question–answer pairs) to make it more useful and instruction-following.
5. RLHF (Reinforcement Learning with Human Feedback) — Humans rank multiple model responses by
   quality; the model is further trained to prefer the responses humans rated as clearer, safer, and
   more helpful.

The result is a model that has absorbed grammar, factual knowledge, and reasoning patterns from its
training data, and can apply them to generate coherent, contextually appropriate text for new prompts
it has never seen before.
```

### Tool 2: [Tool Name] CHATGPT

**Prompt 1 Response:**
```
Generative AI (GenAI): Generative AI is a branch of artificial intelligence focused on creating new content — such as text, images, audio, video, or code — rather than simply analyzing or classifying existing data.

Historical background:** Neural networks date back to the 1950s, with the development of the perceptron. Early neural networks were limited by available computing power and data. In the 2010s, deep learning** emerged, using neural networks with many stacked layers. Deep learning became powerful because its performance could improve significantly with more data, model capacity, and computing resources. This scalability helped make modern Generative AI possible.
Discriminative vs. generative models:** Discriminative models make decisions about existing input data — for example, classifying an email as spam or not spam**. Generative models learn patterns in data and use those patterns to produce new data — for example, **writing a new email in a particular style.

Analogy: Think of a discriminative model as an art critic who can identify whether a painting belongs to a particular style. A generative model is like an apprentice artist** who has studied many paintings and can create a new painting based on the patterns and styles learned.

Foundation models: Modern GenAI systems are often built using **foundation models. These models are trained on massive and diverse datasets and can then be adapted or used for many different tasks without building a separate model from scratch for every task.

In simple words: Generative AI learns from existing data and uses what it has learned to create new content. Deep learning, large datasets, powerful hardware, and modern architectures such as Transformers played a major role in the rise of modern Generative AI.

```

**Prompt 2 Response:**
```
Generative AI model architecture: Generative AI models are designed to learn patterns from large amounts of data and generate new content. Common architectures include **Transformers, GANs (Generative Adversarial Networks), and VAEs (Variational Autoencoders)**. Among these, Transformers are widely used for modern text and multimodal Generative AI systems.

Transformers: A Transformer is a neural network architecture introduced in 2017. It mainly consists of an **input embedding layer, positional encoding, self-attention mechanism, feed-forward neural networks, and output layer**. The input text is first divided into tokens. These tokens are converted into numerical vectors called embeddings. Positional information is added so that the model can understand the order of the words. The self-attention mechanism then determines how important each word is in relation to the other words.

Self-attention: Self-attention allows the Transformer to look at different words in a sentence at the same time and determine their relationships. Unlike older sequential models such as RNNs, a Transformer does not have to process every word strictly one after another during training. This allows it to process many tokens in parallel and makes training more efficient on modern hardware.

Simple example: Consider the sentence **“The dog chased the cat because it was hungry.”** The word **“it”** could refer to the dog or the cat. Through self-attention, the Transformer examines the relationships between **“it,” “dog,” “cat,” “hungry,”** and other words to determine which words are most relevant to understanding the sentence.

GANs: GANs consist of two neural networks: a Generator and a Discriminator. The Generator creates new data, while the Discriminator tries to distinguish between real and generated data. They compete during training, helping the Generator produce increasingly realistic content. GANs are commonly associated with image generation.

VAEs: VAEs consist mainly of an **Encoder** and a **Decoder**. The Encoder converts input data into a compact representation called a latent space, and the Decoder uses this representation to reconstruct or generate new data. VAEs are useful for learning meaningful representations and generating variations of existing data.

Comparison: Transformers are especially suitable for sequences such as text because self-attention captures relationships between tokens and allows efficient parallel processing. GANs use a Generator–Discriminator competition and are commonly used for realistic data generation, especially images. VAEs use an Encoder–Decoder structure and a latent representation to generate new variations of data.

| Model           | Main Architecture               | Main Idea                                           | Common Use                      |
| --------------- | ------------------------------- | --------------------------------------------------- | ------------------------------- |
| **Transformer** | Attention + Feed-forward layers | Understand relationships between tokens             | Text, code, multimodal AI       |
| **GAN**         | Generator + Discriminator       | Two networks compete to improve generation          | Image generation                |
| **VAE**         | Encoder + Decoder               | Learn latent representation and generate variations | Images, representation learning |

In simple words:A Transformer** understands relationships between words using self-attention, a GAN learns through competition between a Generator and Discriminator, and a VAE learns a compressed latent representation and uses it to generate new data.

```

**Prompt 3 Response:**
```
Generative AI applications: Generative AI architecture allows machines to learn patterns from existing data and create new content. Different architectures such as GANs, VAEs, and Transformers are used for different applications depending on the type of data and task.

1. Image generation: Generative AI can create realistic images from text prompts or generate new variations of existing images. GANs use a Generator and Discriminator to create increasingly realistic images, while VAEs can learn a latent representation of images and generate new variations. For example, AI can generate product designs, artwork, or realistic faces.

2. Video generation: Generative AI can create or modify video content, such as generating scenes, animations, and video effects. Transformers can model relationships between video frames and their surrounding context, while other generative architectures can help generate visual content. For example, a user can provide a text description and an AI system can generate a short video based on it.

3. Audio and speech generation: Generative AI can produce human-like speech, music, sound effects, and voice conversions. Transformers can learn patterns in sequences of audio or speech and generate new sequences. For example, text-to-speech systems can convert written text into natural-sounding speech.

4. Code generation: Generative AI can generate computer programs, complete code, explain code, and identify possible errors. Transformers are widely used because programming languages are sequential and contain relationships between different parts of the code. For example, a developer can enter a prompt such as “Create a Python program to calculate factorial,” and the model can generate the required code.

5. Conversational AI: Chatbots and virtual assistants can understand user questions and generate natural-language responses. Transformer-based Large Language Models (LLMs) are commonly used for this application. Self-attention allows the model to consider relationships between words and understand the context of a conversation. Examples include customer-support chatbots, virtual assistants, and educational assistants.

6. Text generation: Generative AI can create emails, summaries, articles, stories, and other written content. **Transformers** are particularly effective because they can learn relationships between words and generate text one token at a time based on the given context.

Architecture and application relationship: The choice of architecture depends on the type of content being generated. **GANs** are well known for realistic image generation, **VAEs** are useful for learning compact representations and generating variations, and **Transformers** are widely used for text, code, conversational AI, and increasingly multimodal content such as audio, images, and video.

| Application           | Example                         | Common Architecture             | How it works                                     |
| --------------------- | ------------------------------- | ------------------------------- | ------------------------------------------------ |
| **Image generation**  | Creating realistic images       | GAN / VAE                       | Learns visual patterns and generates new images  |
| **Video generation**  | Creating scenes or animations   | Transformer + generative models | Learns relationships across frames and content   |
| **Audio/Speech**      | Text-to-speech, music           | Transformer                     | Learns sequential audio patterns                 |
| **Code generation**   | Writing Python/Java code        | Transformer                     | Learns patterns and relationships in source code |
| **Conversational AI** | Chatbots and virtual assistants | Transformer                     | Understands context and generates responses      |
| **Text generation**   | Emails, stories, summaries      | Transformer                     | Predicts and generates tokens based on context   |

**In simple words:** Generative AI architecture acts as the **engine behind different creative applications**. GANs and VAEs are useful for generating and representing visual data, while Transformers are especially powerful for understanding and generating sequential information such as **text, code, speech, and conversations**.

```

**Prompt 4 Response:**
```
Scaling in Large Language Models (LLMs): Scaling means increasing the **model size, training data, and computing resources** used to train an AI model. Research has shown that language-model performance generally improves as these factors increase, following predictable scaling trends over a wide range.

1. Increasing model size: Model size refers to the number of **parameters** in a neural network. A larger model can learn more complex relationships and patterns in language. For example, **GPT-3 has 175 billion parameters**, which helped it perform many language tasks using few-shot prompting. Larger models, however, require more memory, computation, and time for training and deployment.

2. Increasing training data: More high-quality training data gives the model more examples of language, facts, code, and different writing styles. This can improve its ability to generalize to new tasks. However, simply adding more data is not always enough; the **quality and diversity of the data** are also important. Research on compute-optimal training found that model size and the number of training tokens should be balanced rather than increasing only one of them.

3. Increasing compute resources:Training larger models with more data requires powerful hardware such as **GPUs and large distributed computing systems**. More compute allows more mathematical operations to be performed during training. Large-scale training can therefore produce more capable models, but it also increases infrastructure requirements and cost. OpenAI reported that GPT-4 training used AI-optimized supercomputing infrastructure and emphasized predictable scaling of training performance.

GPT-3 vs. GPT-4:GPT-3, released in 2020, was a 175-billion-parameter autoregressive language model and demonstrated that scaling could substantially improve few-shot performance. GPT-4, released in 2023, represented a further scaling milestone. OpenAI described GPT-4 as a large multimodal model and reported stronger performance on a range of professional and academic benchmarks compared with earlier models. OpenAI did **not publicly disclose GPT-4's parameter count**, so it is incorrect to assume a specific GPT-4 parameter number from public information.

4. Challenge — Overfitting: If a model is trained too heavily on limited or repetitive data, it can memorize training examples instead of learning patterns that generalize well. Scaling therefore requires balancing **model size and data quantity/quality**. Research on scaling laws and compute-optimal training shows that the relationship between model size, data, and compute must be carefully managed.

5. Challenge — High cost: Larger models require more GPUs, memory, electricity, storage, and training time. The cost does not end after training because serving a large model to users also requires substantial computing resources.

6. Challenge — Distributed training: Very large models may not fit on a single GPU. Training is therefore distributed across many GPUs and machines using techniques such as **data parallelism and model parallelism**. This introduces challenges such as communication between machines, synchronization, hardware failures, and efficient distribution of workloads. Large-scale parallel training has been an important factor in enabling the growth of modern AI systems.

7. Important lesson from scaling: Bigger is not automatically better. Efficient scaling requires a good balance between **model size, training data, compute, and data quality**. For example, the Chinchilla study found that a smaller 70-billion-parameter model trained on substantially more data could outperform some much larger models, demonstrating the importance of compute-efficient scaling.

In simple words: Scaling an LLM is like expanding a student's learning resources. A **larger brain (model)**, **more textbooks (data)**, and **more study time/resources (compute)** can improve learning. But simply giving the student more books or more time is not enough — the resources must be high quality and properly balanced.

**Summary:** The rise from models such as GPT-3 to GPT-4 illustrates how increasing scale, training methods, data, and compute can produce more capable AI systems. At the same time, scaling creates major challenges involving **cost, data quality, overfitting, memory, and distributed training**.

```

**Prompt 5 Response:**
```
Large Language Model (LLM): A Large Language Model is an AI model trained on a very large amount of text data to understand and generate human-like language. LLMs can perform tasks such as answering questions, summarizing text, translating languages, writing code, and generating conversations. Modern LLMs are mainly based on the **Transformer architecture**.

1. Data collection: The first step is to collect a large and diverse dataset. It can contain books, websites, articles, documents, code, and other text sources. The data is cleaned to remove unwanted, duplicated, or low-quality content.

2. Tokenization: The collected text is divided into smaller units called **tokens**. A token may be a complete word, part of a word, punctuation mark, or other text unit. For example, the sentence **“AI is powerful”** is converted into tokens that the model can represent numerically. These tokens are then converted into numerical IDs that can be processed by the neural network.

3. Transformer architecture: The token IDs are converted into numerical vectors called **embeddings**. Positional information is added so that the model can understand the order of tokens. The Transformer then processes these representations through layers containing **self-attention and feed-forward neural networks**.

4. Self-attention: Self-attention allows the model to determine how strongly different tokens are related to one another. For example, in the sentence **“The student dropped the book because it was heavy,”** the model can use attention to understand that **“it”** is related to **“book.”** This helps the model understand context and relationships within the input.

5. Pre-training: During pre-training, the model learns general language patterns from a huge amount of text. In a typical autoregressive LLM, the model is trained to **predict the next token** based on the previous tokens. For example:

**Input:** “The sun rises in the”
**Expected next token:** “east”

The model makes predictions, compares them with the training data, calculates an error, and adjusts its parameters using optimization techniques. This process is repeated over very large datasets.

**6. Fine-tuning:** After pre-training, the general-purpose model can be fine-tuned using a smaller, carefully prepared dataset for specific tasks. Human-created examples can show the model how to answer questions, follow instructions, summarize information, or perform other desired tasks.

**7. RLHF (Reinforcement Learning from Human Feedback):** RLHF is a method used to make model responses more useful and aligned with human preferences. First, humans compare or rank different model responses. A **reward model** is trained to predict these preferences. The language model is then optimized to produce responses that receive higher rewards according to the learned preference signal.

**8. Final LLM:** After these stages, the resulting model can take a user's prompt, process its tokens using Transformer layers and self-attention, and generate an appropriate response token by token.

**Simple flow:**

**Data Collection → Data Cleaning → Tokenization → Embeddings → Transformer + Self-Attention → Pre-training → Fine-Tuning → RLHF/Preference Optimization → Final LLM**

**Role of Transformer:** The Transformer provides the main architecture that allows an LLM to process language efficiently and understand relationships between tokens. Its self-attention mechanism helps the model focus on relevant parts of the context, while feed-forward layers transform the learned representations.

**In simple words:** Building an LLM is like teaching a student. **Data collection** provides the textbooks, **tokenization** breaks the text into understandable pieces, **pre-training** teaches general language patterns, **fine-tuning** teaches specific tasks and behaviors, and **RLHF** uses human preferences to improve how the model responds.

```

---

## Comparative Analysis

| Criteria                   | CLAUDE    | CHATGPT   | Notes                                                                                   |
| -------------------------- | --------- | --------- | --------------------------------------------------------------------------------------- |
| **Accuracy**               | High      | High      | Both can provide accurate answers, but results depend on the prompt and task.           |
| **Creativity**             | High      | High      | Both can generate stories, ideas, and creative content.                                 |
| **Hallucination**          | Can occur | Can occur | Both may sometimes generate incorrect information; important facts should be verified.  |
| **Reasoning**              | Strong    | Strong    | Both can handle multi-step reasoning, mathematics, and analytical tasks.                |
| **Speed**                  | Fast      | Fast      | Response speed depends on model, workload, and task complexity.                         |
| **Engineering Usefulness** | Strong    | Strong    | Both can assist with programming, debugging, documentation, and technical explanations. |


### Per-Prompt Observations

| Prompt                              | Claude Strengths                                              | ChatGPT Strengths                                                    | Notable Differences                                                                                                 |
| ----------------------------------- | ------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **1. Foundational Concepts**        | Clear explanations and simple analogies                       | Structured and exam-friendly explanation                             | Both explain definitions, history, and concepts clearly.                                                            |
| **2. Architectures (Transformers)** | Good explanation of Transformer components and self-attention | Clear step-by-step explanation with comparisons to GANs and VAEs     | ChatGPT presents the architecture in a more structured format.                                                      |
| **3. Architecture & Applications**  | Connects AI architectures with practical applications         | Provides organized examples across different application areas       | Both cover image, video, audio, code, and conversational AI.                                                        |
| **4. Scaling Impact**               | Explains model size, data, and compute clearly                | Provides detailed discussion of scaling, challenges, and GPT-3/GPT-4 | ChatGPT gives more emphasis to practical challenges such as cost and distributed training.                          |
| **5. LLM Build Process**            | Clearly explains the stages of LLM development                | Provides a detailed step-by-step flow from data collection to RLHF   | ChatGPT gives a more explicit connection between Transformers, self-attention, pre-training, fine-tuning, and RLHF. |


---

## Conclusion

Based on the comparative analysis, both Claude and ChatGPT provide strong performance across the different Generative AI prompts.
Both tools explain foundational concepts, architectures, applications, scaling, and LLM development effectively.
The main differences are in response structure, level of detail, examples, and presentation style.
Their performance can vary depending on the prompt, model version, and complexity of the task.
Overall, the comparison shows that both tools are useful for learning, technical understanding, and engineering-related tasks.

---

## Result

Thus, the prompts for the given Generative AI topics were designed, executed on [Tool 1] and [Tool 2], and their outputs were compared based on accuracy, creativity, hallucination, reasoning, speed, and engineering usefulness.
