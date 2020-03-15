#"Why Should I Trust You" Explaining the Predictions of Any Classifier

##Models:
- LIME: Model level belief, by approximating it with an interpretable model
- SP-LIME: Presenting representative predictions and explanations, by submodular optimization

##Typical Problems:
- Trust individual predictions. Like medical diagnosis or terrorism detection whose result could be catastrophic
- Evaluate as a whole. Real-world data is often significantly different. Suggest users which instances to inspect. Especially for large datasets.

##Procedure
###Relationship Between Components of A Sample and The Prediction (features of explainers)
- step 1: Output of a model: flu, feature vector
- step 2: LIME
- step 3: Prediction:flu; Evidence:sneeze, headache; Evidence against it:no fatigue
- problems and what can be done by x models
    + data leakage (in some datasets, patient IDs are important)
    + dataset shift (20 newsgroups dataset)
- expalain particular predictions to compare different models 
###Desired Characteristics for Explainers
- Interpretable (e.g. qualitative understanding between input and response)
    + User's limitations
    + Should be easy to understand (input variables in the explanation are not equal to the features)
- Local Fielity (correspond to data points close to the predicted instance)
- Model-Agnostic (treat the original model as a black box)
- Global Perspective (select a few explanations to present to the user, such that they are representative of the model)