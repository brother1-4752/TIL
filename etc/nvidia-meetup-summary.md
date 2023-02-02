# NVIDIA 세미나 발표자료

# LLM이란?

- **텍스트 데이터의 대규모 데이터 세트에 대해 훈련된 일종의 AI모델**
- **목표 : 인간과 유사한 텍스트 생성**
    - **Ex. ChatGPT**

<aside>
💡 **ChatGPT는 LLM으로서, 입력을 바탕으로 인간과 유사한 텍스트를 생성하는 기능을 한다. 텍스트 데이터의 대규모 데이터 세트에 대해 교육을 받았으며 광범위한 주제와 질문을 이해하고 응답할 수 있다.**

</aside>

# LLM 학습 : NeMo와 Megatron

## 1-1. NeMo

- **AI모델 개발을 위한 오픈 소스 Toolkit**
- **Collection of pre-built neural network**
- **Easy to use with High level API**

## 1-2. NeMo와 비슷한 Toolkit

- **TensorFlow**
- **Hugging Faces’s Transformers**
- **AllenNLP**

## 1-3. 각 Toolkit의 장단점

**TensorFlow:**

- **Strengths: Widely-used, large community, pre-trained models, support for distributed training, wide range of tools**
- **Weaknesses: it can require more code and a deeper understanding of the underlying mechanics to use it effectively., Complex API, `less efficient for certain types of models`**

**Hugging Face's Transformers:**

- **Strengths: Specifically built for NLP, designed to be more user-friendly, with simpler APIs and pre-built modules and models. pre-trained models, support for different languages and models architectures**
- **Weaknesses: `Limited to NLP`, relatively new library**

**AllenNLP:**

- **Strengths: Built on Pytorch, focused on NLP, easy to use, pre-built models and modules for various NLP tasks**
- **Weaknesses: `Limited to NLP`, fewer pre-built models and modules**

**NeMo:**

- **Strengths: Modular design, pre-built neural modules, support for distributed training, support for speech and language understanding tasks, designed to be more user-friendly, with simpler APIs and pre-built modules and models.**
- **Weaknesses: Relatively new, `limited to Pytorch`, may not be as well-suited for large-scale distributed training and deployment as Tensorflow,  텐서플로우만큼 `사전 구축된 모델과 모듈이 많지 않을 수 있으며, 이는 일부 사용자에게 접근성을 떨어뜨릴 수 있다.`**

## 2-1. Megatron이란?

- **메가트론(Megatron)은 NeMo 위에 세워진 대형 언어 모델을 교육하기 위한 `라이브러리`이다. 여러 GPU와 여러 기계에 걸쳐 언어 모델의 훈련을 확장하도록 설계되어 수십 억 개의 매개 변수로 모델을 훈련할 수 있다. `메가트론의 주요 초점은 라이브러리의 확장성과 성능`에 있다.**
- **메가트론은 `모델 병렬화`라는 기술을 사용하여 대형 모델을 여러 GPU에 걸쳐 분할하고 이들 간의 통신을 처리한다. 이를 통해 수십 억 개의 매개 변수로 모델을 효과적으로 훈련할 수 있다. 또한 사용자가 최소한의 코드 변경으로 모델을 교육할 수 있는 PyTorch와 같은 인기 있는 딥 러닝 프레임워크와 호환되는 간단하고 사용하기 쉬운 API를 제공한다.**
- **이 외에도 메가트론은 정밀도가 낮은 데이터 유형을 사용하여 훈련 과정의 속도를 높이는 데 사용되는 최적화 기법인 `혼합 정밀 훈련`을 지원한다. 이는 모델의 메모리 요구 사항을 줄이고 교육 프로세스를 가속화하는 데 도움이 될 수 있다.**
- **또한 메가트론은 여러 기계에 걸쳐 모델의 훈련을 확장할 수 있는 `분산 훈련`도 지원한다. 이 기능은 매우 큰 모델로 작업하거나 많은 양의 데이터로 작업할 때 특히 유용합니다.**
- **요약하자면, 메가트론은 여러 GPU와 여러 기계에서 대규모 언어 모델을 효과적이고 효율적으로 교육할 수 있는 NeMo 위에 구축된 라이브러리이다. 모델 병렬화와 혼합 정밀 훈련을 사용하여 훈련 과정의 속도를 높이고 분산 훈련에 대한 지원도 제공한다.**

## 2-2. 모델 병렬화 개념

- **대규모 언어 모델을 교육할 때 모델의 매개 변수가 단일 GPU의 메모리에 맞지 않을 수 있으며, 이 경우 모델을 효과적으로 교육하기 위해 여러 GPU에 걸쳐 모델을 분할해야 한다. 이 기술을 `모델 병렬화`라고 한다.**
- **모델 병렬화는 여러 GPU에 걸쳐 딥 러닝 모델의 훈련을 확장하는 데 사용되는 또 다른 기술인 `데이터 병렬화와 다르다는 점`에 주목할 필요가 있다. 데이터 병렬화에서는 동일한 모델이 여러 GPU에 복제되며 각 GPU는 `데이터의` 다른 부분 집합을 처리한다.**

## 2-3. 관련 용어

- **역전파**
    - **When training a model using backpropagation and model parallelism, each GPU calculates the gradients for the subset of model parameters stored on that GPU. These gradients are then passed to other GPUs, where they are used to update the corresponding subset of model parameters.**
    - **This means that during the training process, each GPU is responsible for computing gradients for the subset of model parameters that it holds, and then these gradients are communicated between GPUs `to update the model parameters.` By splitting the model across multiple GPUs, it allows for larger models to be trained and also allows for faster training as the computation can be done in parallel across GPUs. However, this approach requires more complex communication and coordination between GPUs, which can add some overhead to the training process.**
- **그레디언트**
    - **In the context of machine learning, a gradient is a vector of partial derivatives of a function. In the case of neural networks, the function is typically the loss function, and the partial derivatives are taken with respect to the model parameters. `The gradient represents the rate of change of the loss function with respect to the model parameters`, and it is used to update the model parameters during training.**
    - **More specifically, `in deep learning, gradients are used in the backpropagation process, which is used to train neural networks.` During the forward pass of the neural network, the input is processed through the layers of the network, and the output is compared to the desired output (or target) to calculate the loss. During the backward pass, the gradient of the loss with respect to the model parameters is calculated, and this gradient is used to update the model parameters using an optimization algorithm such as stochastic gradient descent ([SGD)](https://www.notion.so/NVIDIA-41d05f5114f346948d373275efd0d089). The goal is to minimize the loss function `by updating the parameters in the direction opposite to the gradient.`**
        - **SGD(Stochastic Gradient Descent)**
            - **구현 코드**
                
                ```python
                Copy code
                import torch
                
                # Define the model and the loss function
                model = ...
                loss_fn = ...
                
                # Define the optimizer
                optimizer = torch.optim.SGD(model.parameters(), lr=0.01)
                
                # Train the model
                for inputs, labels in training_data:
                    # Forward pass
                    output = model(inputs)
                    loss = loss_fn(output, labels)
                
                    # Zero gradients
                    optimizer.zero_grad()
                
                    # Backward pass
                    loss.backward()
                
                    # Update parameters
                    optimizer.step()
                
                ```
                
                - **In this example, `model` is the neural network, `loss_fn` is the loss function used to calculate the error, and `optimizer` is an instance of the `torch.optim.SGD` class. The `lr` argument passed to the constructor of the `SGD` class is the learning rate, which determines the step size of the updates to the model's parameters.**
                - **The training loop iterates over the training data, and for each iteration, it performs a forward pass through the model to generate an output and calculate the loss. Then it calls `optimizer.zero_grad()` to clear the gradients, `loss.backward()` to calculate the gradients and finally `optimizer.step()` to update the model's parameters using the gradients and the learning rate.**
                - **It's worth noting that this is just a simple example of how SGD can be implemented. In practice, there are many variations and modifications that can be made to the algorithm to improve its performance such as, using different learning rates, implementing momentum, nesterov momentum, or using learning rate schedules.**

# FasterTransformer and Triton

- **FastTransformer**는 언어 번역, 언어 이해 및 텍스트 생성과 같은 효율적이고 정확한 자연어 처리(NLP) 작업을 위해 설계된 `**신경망 아키텍처**`입니다. 이것은 NLP에서 널리 사용되는 트랜스포머 아키텍처의 extenstion이다. Fast Transformer는 주의 메커니즘과 피드 포워드 레이어를 재설계하고 보다 효율적인 데이터 레이아웃을 사용하여 Transformer의 계산 복잡성을 줄입니다. 이를 통해 높은 정확도를 유지하면서 더 빠른 훈련과 추론 시간을 가능하게 한다.
- **Triton**은 NVIDIA가 개발한 딥 러닝 모델을 배포하기 위한 `**서버 측 플랫폼**`이다. 높은 성능, 낮은 지연 시간 및 높은 처리량으로 머신 러닝 모델을 배포하고 서비스할 수 있습니다. Triton은 TensorFlow, PyTorch 및 ONNX를 포함한 광범위한 모델 및 프레임워크를 지원하며, 온프레미스 서버, 에지 장치 및 클라우드 기반 인프라와 같은 다양한 플랫폼에 모델을 배포하는 데 사용할 수 있다. 트리톤은 또한 GPU와 같은 자원의 즉각적인 스케일링을 수행하여 다양한 부하와 트래픽을 처리하는 데 사용될 수 있다.