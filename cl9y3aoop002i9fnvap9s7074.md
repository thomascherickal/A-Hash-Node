---
title: "What’s New in TensorFlow 2.0"
datePublished: Fri Oct 09 2020 02:15:17 GMT+0000 (Coordinated Universal Time)
cuid: cl9y3aoop002i9fnvap9s7074
slug: whats-new-in-tensorflow-2-0-55a3132b188d
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667299871169/QUx8KFm7BH.jpeg

---

#### New Features in TensorFlow 2.0

*Support my writing*

**Join Medium.com as a member** through the link below.

[**https://thomascherickal.medium.com/membership**](https://thomascherickal.medium.com/membership)

TensorFlow 2.0 is coming soon. And boy, are we super-excited! TensorFlow first began the trend of open-sourcing AI and DL frameworks for use by the community. And what has been the result? **TensorFlow has become an entire ML ecosystem for all kinds of AI technology. Just to give you an idea, here are the features that an absolutely incredible community has added to the original TensorFlow package:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299856464/Fc99b1dLmg.png)

**From Medium.com**

### Features of TensorFlow contributed from the Open Source Community

TensorFlow started out as a difficult-to-learn framework for deep learning from Google. With one difference — **it was open-sourced.** That may appear as stupidity for a commercial company that focuses on profits, but it was the right thing to do. **Because the open source community took it up as their own property and ported it to nearly every platform available today including mobile, web, IoT, embedded, Edge Computing** and so much more. And even more: **from Python and C, it was ported to JavaScript, C++, C#, Node.js, F#, React.js, Go, Julia, R, Rust, Android, Swift, Kotlin, and even a port to Scala, Haskell, and numerous other coding languages.** Then, after that complete conquest, Google went into the next level for optimization — **hardware.**

Which means — now we have CUDA (library for executing ML code on GPUs) v8-v9-v10 (9.2 left out), GPGPU, GPU-Native Code, TPU (Tensor Processing Unit — custom hardware provided by Google specially designed for TensorFlow), Cloud TPUs, FPGAs (Field-Programmable Gate Arrays — Custom Programmable Hardware), ASIC (Application Specific Integrated Circuits) chip hardware specially designed for TensorFlow, and now MKL for Intel, BLAS optimization, LINPACK optimization (the last three all low-level software optimization for matrix algebra, vector algebra, and linear algebra packages), and so much more that I can’t fit it into the space I have to write this article. To give you a rough idea of what the TensorFlow architecture looks like now, have a look at this highly limited graphic:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299858335/K806tS9n4.png)

Source: planspaces.org

Note: **XLA stands for A(X)ccelerated Linear Algebra compiler still in development that provides highly optimized computational performance gains.**

### And Now TensorFlow 2.0

This release is expected shortly in the next six months from Google. Some of its most exciting features are:

1.  **Keras Integration as the Main API instead of raw TensorFlow code**
2.  **Simplified and Integrated Workflow**
3.  **Eager Execution**
4.  **More Support for TensorFlow Lite and TensorFlow Edge Computing**
5.  **Extensions to TensorFlow.js for Web Applications and Node.js**
6.  **TensorFlow Integration for Swift and iOS**
7.  **TensorFlow Optimization for Android**
8.  **Unified Programming Paradigms (Directed Acyclic Graph/Functional and Stack/Sequential)**
9.  **Support for the new upcoming WebGPU Chrome RFC proposal**
10.  **Integration of tf.contrib best Package implementations into the core package**
11.  **Expansion of tf.contrib into Separate Repos**
12.  **TensorFlow AIY (Artificial Intelligence for Yourself) support**
13.  **Improved TPU & TPU Pod support, Distributed Computation Support**
14.  **Improved HPC integration for Parallel Computing**
15.  **Support for TPU Pods up to v3**
16.  **Community Integration for Development, Support and Research**
17.  **Domain-Specific Community Support**
18.  **Extra Support for Model Validation and Reuse**
19.  **End-to-End ML Pipelines and Products available at TensorFlow Hub**

**And yes — there is still much more that I can’t cover in this blog.**

Wow — that’s an Ocean! What can you Expand Upon?

Yes — that is an ocean. But to keep things as simple as possible (and yes — stick to the word limit — cause I could write a thousand words on every one of these topics and end up with a book instead of a blog post!) we’ll focus on the most exciting and striking topics (**ALL** **are exciting — we’ll cover the ones with the most scope for our audience**).

### 1\. Keras as the Main API to TensorFlow

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299860567/qFGOHxMe6.png)

From [www.keras.io](http://www.keras.io)

**Earlier, comments like these below were common on the Internet:**

> *“TensorFlow is broken” — Reddit user*

> *“Implementation so tightly coupled to specification that there is no scope for extension and modification easily in TensorFlow” — from a post on Blogger.com*

> *“We need a better way to design deep learning systems than TensorFlow” — Google Plus user*

Understanding the feedback from the community, Keras was created as an open source project designed to be an easier interface to TensorFlow. Its popularity grew very rapidly, and now nearly 95% of ML tasks happening in the real world can be written just using Keras. Packaged as ‘Deep Learning for Humans’, Keras is simpler to use. Though, of course, **PyTorch gives it a real run for the money as far as simplicity is concerned!**

In TensorFlow 2.0, Keras has been adopted as the main API to interact with TensorFlow. Support for pure TensorFlow has not been removed, and thus TensorFlow 2.0 will be completely backwards-compatible, including a conversion tool that can be used to convert TensorFlow 1.x to TensorFlow 2.0 where implementation details differ. Kind of like **the Python tool 2to3.py**! So now, **Keras is the main API for TensorFlow deep learning applications** — which takes out a huge amount of unnecessary complexity burdens from the ML engineer.

### 2\. Simplified and Integrated WorkFlow

There is a step-by-step simpler and extremely flexible workflow process for designing deep learning models: (visit [https://medium.com/tensorflow/whats-coming-in-tensorflow-2-0](https://medium.com/tensorflow/whats-coming-in-tensorflow-2-0) for more details)

1.  Use **tf.data** for data loading and preprocessing or use **NumPy**.
2.  Use **Keras** or **Premade Estimators** to do your model construction and validation work.
3.  Use **tf.function** for DAG graph-based execution or use **eager execution** ( a technique to smoothly debug and run your deep learning model, on by default in TF 2.0).
4.  For TPUs, GPUs, distributed computing, or TPU Pods, utilize **Distribution Strategy** for high-performance-computing distributed deep learning applications.
5.  **TF 2.0 standardizes SavedModel as a serialized version of a TensorFlow graph for a variety of different platforms** like Mobile, JavaScript, Edge, Lite, TensorBoard, TensorHub, and TensorServing. This makes it easier to move models around different architectures. This was one feature that was highly necessary compared to the older scenario.

This means that now even novices at machine learning can perform deep learning tasks with relative ease. **And of course, did we mention the wide variety of end-to-end pluggable deep learning solutions available at TensorHub and on the Tutorials section**? **And guess what — they’re all free to download and use for commercial purposes.** Google, you are truly the best friend of the open source community!

### 3\. Expanded Support for Mobile (Android and iOS), Web (JavaScript), TF Lite, TF Edge and IoT

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299861863/S3XDKCyGV.jpeg)

From Medium.com

In all the above platforms, where computational and memory resources are scarce, there is a common trend in TF 2.0 that extends over most of these platforms.

1.  Greater support for various ops in TF 2.0 and several deployment techniques
2.  SIMD+ support for WebAssembly
3.  Support for Swift (iOS) in Colab.
4.  Increased support for data input pipelines, and data visualization libraries in JavaScript.
5.  A smaller and lighter footprint for Edge Computing, Mobile Computing and IoT
6.  Better support for audio and text-based models
7.  Easier conversion of trained TF 2.0 graphs
8.  Increased and improved mobile model optimization techniques

As you can see, Google knows that Edge and Mobile is the future as far as computing is concerned, and has designed its products accordingly. TF Mobile should be replaced by TF Lite soon.

### 4\. Unified Programming Models and Methodologies

There are two/three major ways to code deep learning networks in Keras. They are:

1.  **Symbolic or Declarative APIs**
2.  **Imperative APIs / Subclassing**

We shall look at both of them in turn, in a very **minute** way. For more on this topic, visit [https://medium.com/tensorflow/what-are-symbolic-and-imperative-apis-in-tensorflow-2-0](https://medium.com/tensorflow/what-are-symbolic-and-imperative-apis-in-tensorflow-2-0)

#### Symbolic/Declarative/Graph-Based/Functional API

We build models symbolically by describing the structure of its DAG (Directed Acyclic Graph) or a sequential stack. This following image is an example of Keras code written symbolically.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299863733/GGzP4zDCY.png)

From Medium.com TensorFlow publication

This looks familiar to most of us since this is how we use Keras usually. The advantages of this process are that it’s easy to visualize, has debugging errors usually only at compile time, and corresponds to our mental model of the deep learning network and is thus easy to work with.

#### Stack-Based/Subclassing/Imperative API

The following code is an example of the Sequential paradigm or subclassing paradigm to building a deep learning network:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299865366/P2Y9QM-1Qq.png)

From Medium.com TensorFlow publication (code still in development)

Rather similar to Object Oriented Python, this style was first introduced into the deep learning community in 2015 and has since been used by a variety of deep learning libraries. TF 2.0 has complete support for it. Although it appears simpler, it has some serious disadvantages.

Imperative models are not a data structure that is transparent but an opaque class instead. You are prone to many errors at runtime following this approach. As a deep learning practitioner, you are obliged to know both symbolic as well as imperative and subclassing methodologies of coding your deep neural network. For example, recursive or recurrent neural networks cannot be defined by the symbolic programming model. So it is good to know both. But be aware of the disparate advantages and disadvantages of them!

### 5\. TensorFlow AIY

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299867250/3bf-sp1Ka5.jpeg)

From slideshare.com

This is a brand new offering from Google and other AI companies such as Intel. **AIY stands for Artificial Intelligence for Yourself (a play on DIY — Do It Yourself) and is a new marketing scheme from Google to show consumers how easy it is to use TensorFlow in your own DIY devices to create your own AI-enabled projects and gadgets. This is a very welcome trend, since it literally brings the power of AI to the masses, at a very low price.** I honestly feel that now the day is nearing when schoolchildren will bring their AIY projects for school exhibitions and that the next generation of whiz kids will be chock full of AI expertise and development of new and highly creative and innovative AI products. This is a fantastic trend and now I have my own to-buy-and-play-with list if I can order these products on Google at a minimal shipping charge. So cool!

### 6\. Guidelines and New Incentives for Community Participation and Research Papers

We are running out of the word limit very fast! I hoped to cover TPUs and TPU Pods and Distributed Computation, but for right now, this is my final point. Realizing and recognizing the massive role the open source community has played in the development of TensorFlow as a worldwide brand for deep learning neural nets, the company has set up various guidelines to introduce domain-specific innovation and the authoring of research papers and white papers from the TensorFlow community, in collaboration with each other.

In fact, when I read more of the benefits of participating in the TensorFlow community open source development process, I could not help it, **I joined the TensorFlow development community, myself as well!**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299869133/pD7QUKFUZK.png)

A freelance developer and writer contributing to TensorFlow!

**Who knows — maybe, God-willing, one day my code will be a part of TensorFlow 2.0/2.x! Or — even better — there could be a research paper published under my name with collaborators, perhaps. The world is now built around open source technologies, and as a developer, there has never been a better time to be alive!**

### In Conclusion

So don’t forget, on the day of writing this blog article, 31th January 2019, TensorFlow 2.0 is yet to be released, but since its an open source project, there are no secrets and Google is (literally) being completely ‘open’ about the steps it will take to take TF further as the world market leader in deep learning.

Cheers!

#### Support My Writing

**Support my writing.** **Join Medium** to read the best content on the web through the link below and 50% of your membership fee supports me every month. A sincere thanks to all my wonderful subscribers who help me and support my writing every month.

Join Medium with my referral link below — Thomas Cherickal

[**https://thomascherickal.medium.com/membership**](https://thomascherickal.medium.com/membership)

God bless.

#### Coffee!

If you enjoyed this article, do buy me a coffee every month for 2 USD:

[https://ko-fi.com/thomascherickal](https://ko-fi.com/thomascherickal)