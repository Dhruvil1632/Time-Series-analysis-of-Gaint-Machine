# Time-Series-analysis-of-Gaint-Machine
Industry has very high rated machine , if they will damage then company has to pay a lot. Based on some previous behavior of machine, using machine learning I predicted
when machine goes down or when anomaly has arise.Base on this results company
prefer some precautions to reduce the chance of damages. 
![](data:image/png;base64,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)
