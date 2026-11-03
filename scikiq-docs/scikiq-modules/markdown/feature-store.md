---
hidden: true
---

# Feature Store

Features are input for machine learning models. The most efficient way to use them across an organization is in a feature store that automates the data transformations, stores them and makes them available for training and inference.

ML projects and application various feature-specific challenges are:

1\.     Often, features are not reused across teams and different ML applications in an organization, and some teams may define and use features differently.

2\.     Additional effort is needed to provide each ML model with the required features.

Feature stores rectify these issues by improving consistency of definition and increasing efficiency for data science teams.

Feature stores allow teams to reuse features across data science projects and ML models effectively, increasing the efficiency and scalability of their MLOps process.

&#x20;

What Is a Feature?

In ML, a predictive model learns to make predictions based on past examples. A “feature” is an attribute that is used to describe each example.

<figure><img src="../../.gitbook/assets/image (1136).png" alt=""><figcaption></figcaption></figure>

Each row in the table is a data instance that can be used for training or inference. The columns represent individual features, and each cell is a feature value.

The features that are used as training data for ML models are created during a process called feature engineering. In this process, a data scientist applies transformations to raw data in order to create features that can be consumed by an ML model.

&#x20;

What Is a Feature Store?

An feature store is a central store that manages features specifically prepared for the data science process. By making it easy to search and find features, they can easily be reused across projects, improving efficiency, governance and model velocity (end-to-end model development _and_ deployment process rapidly, repeatedly, and consistently – from data engineering, feature engineering, algorithm selection, hyperparameter tuning, validation, deployment, to monitoring).

Most ML or DL models require hundreds to thousands of features that may be processed differently depending on the data type. However, managing a large number of features is not straightforward, and the same set of features may apply to different ML use cases.

For instance, a Bank uses two different ML models: Model A and Model B. Model A uses the feature to predict the credit score of a particular customer. At the same time, a different model, Model B, uses the same feature to predict the probability that this customer will upgrade to a certain product when approached by the Bank. When the same type of features is used for several applications, it makes sense to reuse features across these models.

&#x20;

Feature Store Components

Core Components of a Feature Store

1\.     Feature Repository: A centralized storage system that maintains features and their metadata, including definitions, transformations, and lineage.

2\.     Feature Pipeline: Processes for transforming raw data into features, which can be scheduled to run continuously or on demand.

3\.     Feature Registry: A catalog that documents all available features with metadata, allowing for discovery and reuse.

4\.     Serving Layer: Infrastructure that provides low-latency access to features for online inference.

5\.     Offline Store: Storage for batch feature retrieval typically used in training.

A modern feature store consists of three main components—transformation, storage, and serving:



<figure><img src="../../.gitbook/assets/image (1137).png" alt=""><figcaption></figcaption></figure>

&#x20;ML models usually require transformations of raw data into features that the ML model can consume. For instance,

1\.     ML/DL models do not handle features well that are represented as categories or labels (e.g. gender or color). Therefore, you need to transform this categorical data into a more suitable format.

2\.     In case of long text, these are needed to be handled in vectors format.

3\.     Other transformations include standardization of data and calculated values.

4\.     New feature creation based on business logic, by combining raw features (addition, multiplication etc.)

5\.     Even some times target variable creation based on business logics and multiple features.

&#x20;

Feature stores orchestrate these feature transformations, and there are mainly two types:

1\.     Batch transformations are applied only to data at rest and can be found in a database, data warehouse, or data lake. A typical example of this kind of data is historical customer data that can be found in a table.

&#x20;

2\.     Streaming transformations are applied to data in motion or streaming sources. This means that the data is transformed online as it moves through the feature store pipeline. This kind of data is more recent as compared to data in a database or data warehouse. For example, data that must have streaming transformations applied would include the number of clicks on a landing page per user in the last thirty minutes or the number of views per listing in the past hour per user.

&#x20;

Storage

At a high level, a feature store is a warehouse of feature data used by ML operations. A feature store differs architecturally from a traditional data warehouse in the sense that it consists of a two-part database:

1\.     An “offline database” is primarily intended for batch predictions and model training. The database stores large amounts of historical features for training purposes of ML models.

Example use case: A data scientist training a model to predict customer churn would use the offline database to access historical customer behavior data, allowing them to create and test features over extended time periods.

2\.     The second database, called the “online database”, serves online features at low latency to trained models that are already in production. This online database satisfies the need to provide the most up-to-date features to the predictive models.

Example use case: An e-commerce recommendation system would use the online database to quickly retrieve up-to-date user behavior features to generate personalized product recommendations in real-time as a customer browses the website.

&#x20;

Serving

The transformed data that has been stored in the feature store can now be retrieved and provided to ML/DL models for training or once they are in production. This process is referred to as “serving”. This step is essential because it ensures that the correct feature data is constantly used.

For model training, offline data from the offline database is retrieved and used. For serving features to a model in production, the data is served from the online database through a high-performance and low-latency API.

&#x20;

Key Benefits of Feature Stores

1\.     Feature Reusability and Sharing

o    Enables teams to reuse features across projects

o    Prevents redundant feature engineering work

o    Establishes a standardized feature catalog

2\.     Consistency Between Training and Serving

o    Eliminates training-serving skew by using identical transformations

o    Ensures model performance in production matches expectations

&#x20;

3\.     Efficient Feature Computation

o    Prevents redundant calculations through caching mechanisms

o    Optimizes resource utilization for feature generation

4\.     Reliable Feature Access

o    Provides high-availability, low-latency access for online serving

o    Enables scalable batch retrieval for model training

5\.     Feature Governance and Documentation

o    Maintains feature lineage and versioning

o    Tracks usage patterns and impact on models

o    Documents feature definitions and business context

6\.     Simplified ML Operations

o    Streamlines deployment of new features and models

o    Enables monitoring of feature drift and distribution changes



Detailed Feature Store Product Requirements

[https://docs.google.com/spreadsheets/d/1bA073yjges8EUNPr2sKiBqCoJHDNCl\_fs2GQ23rVXlY/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1bA073yjges8EUNPr2sKiBqCoJHDNCl_fs2GQ23rVXlY/edit?usp=sharing)

&#x20;

&#x20;

&#x20;

&#x20;

&#x20;

Other Links

[https://www.featurestore.org/](https://www.featurestore.org/) = Featurestore.org is a global community for data science professionals to share ideas and learn about feature stores and information on various open-source and proprietary feature store platforms.

&#x20;

H20 Feature Store Services and Architecture:

[https://docs.h2o.ai/featurestore/get-started/architecture#high-level-architecture](https://docs.h2o.ai/featurestore/get-started/architecture#high-level-architecture)\
<br>

[https://docs.h2o.ai/featurestore/get-started/architecture#technical-components](https://docs.h2o.ai/featurestore/get-started/architecture#technical-components)\
\
Vertex AI Feature Store

[https://cloud.google.com/vertex-ai/docs/featurestore/latest/overview](https://cloud.google.com/vertex-ai/docs/featurestore/latest/overview)\
<br>

Sagemaker Feature Store

[https://docs.aws.amazon.com/sagemaker/latest/dg/feature-store.html](https://docs.aws.amazon.com/sagemaker/latest/dg/feature-store.html)\
<br>

Dataiku Feature Store

[https://knowledge.dataiku.com/latest/mlops-o16n/feature-store/tutorial-building-feature-store.html](https://knowledge.dataiku.com/latest/mlops-o16n/feature-store/tutorial-building-feature-store.html)\
<br>

