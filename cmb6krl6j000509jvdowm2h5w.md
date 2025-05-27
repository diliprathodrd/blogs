---
title: "GenAI - Magic under the hood"
datePublished: Tue May 27 2025 13:51:32 GMT+0000 (Coordinated Universal Time)
cuid: cmb6krl6j000509jvdowm2h5w
slug: genai-magic-under-the-hood
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1748346200768/43efb682-f62b-4462-a6f5-95aa03ef0745.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1748353821843/6a3a3ef3-7087-4346-adb6-3e93681d2cb8.png
tags: python, hiteshchoudharylco, hiteshchoudhary, genai, chaicode, chai-code

---

I was very much curious about AI since openAI launched chatGPT. I did research about it but didn’t cleared my concept though I use chatGPT and Gemini in my day to day works.

Recently I joined GenAI cohort by @[Hitesh Choudhary](@hiteshchoudharylco) and @[Piyush Garg](@piyushgarg) and started my journey towards learning generative AI. lets breakdown the things and understand the magic under the hood.

## 🧠What is generative AI?

In simple words, generative AI is generating something using AI (Artificial Intelligence).

In search engine we get the results based on keyword we provide but generative AI model generates response based on our requirements. It reduces the multiple option dilemma and give us most accurate and appropriate answer based on our search term.

OpenAI first introduced first model named chatGPT, GPT stands for Generative Pre Trained Transformer. Gemini and Claude are also similar GPT’s. These GPT’s or models are not magic, they just generates response based on pre-trained data. Though OpenAI introduced chatGPT, first generative AI model, but google was already using this kind of generative transformer for google translate.

> [Click here](https://arxiv.org/pdf/1706.03762) for reference paper by Google.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1748348054654/a451bc87-0455-46dc-8771-93cea0db5151.png align="center")

## 🗨️How Google used transformer architecture for Google Translate?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1748348666963/f36c869f-7b3d-4c2b-a07d-627442451a9a.png align="center")

## 🏷️Tokenization

It takes input from input box and process it to translate the input string into desired language. These transformers treat these input strings as tokens. every GPT models have their own algorithms to generate these tokens from input string. collection of tokens is known as sequence. All these GPT’s requires high computing power as they need to process lot of tokens and generate lot of tokens. Thats why most of the models give limited free tokens to use.

To compute the meaning of tokens, every models have their own algorithms to convert these tokens into numbers. Once tokens or sequences converted into numbers its easy for these models to process and compute the result. This process is known as `tokenization`

> If you want to see visualize tokenization, [click here](https://tiktokenizer.vercel.app/) and try with your input string. you can see tokens generated from input stings and the numbers for each token generated.

## 📈Vector Embedding

Vector Embedding gives meaning to generated numbers. vector embeddings are numeric representation of data that captures semantic relationship and similarities

### Why Vector Embeddings are important?

To plot the real meaning of generated numbers.

e.g. when we translate `how are you` it translates like `आप कैसे हैं` instead of `आप हैं कैसे` , this happens because of vector embedding.

## Positional Encoding

Positional Encoding adds information in vector embedding about the positions of the token. We can imagine it like indexing in array.

e.g.

1. Dog chases Cat
    
2. Cat chases Dog
    

in above case, for both the sequences have same token but the meaning is very different.

Also lets consider one more example.

1. The River Bank
    
2. The SBI Bank
    

In both the sequences, token for bank will be same but the meaning of bank in each sequence is different. This is called multihead attention.

There are 2 phases of GPT’s

1. Training
    
2. Inferencing
    

### Training

* In training phase, back propagation is done to train the model.
    

### Inferencing

* Inferencing is nothing but the actual use of model.
    

## 🥅Fine tuning

When initially model is build, we need to train that model. The training is done using back propagation. for example `2+2`. The actual answer for this is `4` but model may give the wrong answer. So we will calculate the difference between actual answer and answer given by model which is also known as loss. back propagation is done till the loss is nearly 0. That model we can say as trained model.

> [CLICK HERE](https://courses.chaicode.com/learn/batch/GenAI-with-Python-2) to join GetAI Cohort with Python - 2.0 and follow to ride the journey of this cohort with me.