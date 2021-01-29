# coursera-machine-learning-Andrew-Ng-
coursera machine learning(Andrew Ng)<br>
https://www.coursera.org/learn/machine-learning#syllabus


<h3>1 week</h3><br>
Machine learning algorithm: Supervised learning, Unsupervised learning<br>
-Supervised learning: 작업을 수행할 수 있는 방법을 컴퓨터에게 가르치는 것이 핵심<br>
-Unsupervised learing: 컴퓨터가 스스로 학습하도록 유도<br>
<br>
<h3>What is Supervised learning?</h3><br>
Supervised learning은 우리가 알고리즘에 데이터셋을 주는데 각 데이터에 '정답'이 포함되어 있는것이다.<br>
알고리즘의 역할은 그 '정답'을 더 많이 만들어 내는것. 이것은 regression problem(회귀문제)이라고도함.
<br>회귀문제: 연속된 값을 가진 결과를 예측하려 하는것<br><br>
Breast Cancer (malignant, benign) -> Classification : Discrete valued output (0 or 1)<br>
Tumor size에 따른 양성, 악성 판별문제.
<img src="https://user-images.githubusercontent.com/67510613/105625656-03513800-5e6e-11eb-8c6b-490fbd461fbc.JPG">
Tumor size, age에 따른 양성, 악성 판별문제.
<img src="https://user-images.githubusercontent.com/67510613/105625741-8c686f00-5e6e-11eb-9020-b89b6efd85ed.JPG">
<br><br>
이렇게 1,2개 특성이 아니라 무한대의 특성을 다루려면 어떻게해야하는가? <br>
-> Support Vector Machine Algorithm<br><br>
<hr>
<h3>Supervised Learning</h3><br>
In supervised learning, we are given a data set and already know what our correct output should look like, <br>
having the idea that there is a relationship between the input and the output.<br><br>

Supervised learning problems are categorized into "regression" and "classification" problems. In a regression<br> problem, we are trying to predict results within a continuous output, meaning that we are trying to map input <br>
variables to some continuous function. In a classification problem, we are instead trying to predict results <br>
in a discrete output. In other words, we are trying to map input variables into discrete categories. <br>
<hr><br>


<h3>What is Unsupervised learning?</h3><br>
데이터 레이블이 주어지지않는다. 이것으로 뭘할지 또 각 데이터가 무엇인지 알 수 없다.<br>
1. clustering algorithm
<img src="https://user-images.githubusercontent.com/67510613/105629761-3b657480-5e88-11eb-95f4-b2bd4782a045.JPG">
스스로 그룹화하는 것?<br><br>


2. Cocktail party problem<br>
여러 잡음이 존재하고 다양한 오디오를 각각 분리한다.<br>
[W,s,v]=svd((repmat(sum(x.*x,1),size(x,1),1).*x)*x');<br>
*수업에서 Octave programming environment를 사용할 것임.<br>
svd함수는 특이값분해(singular value decomposition)의 약자_octave내장함수임
<hr>
<h3>Unsupervised Learning</h3><br>
Unsupervised learning allows us to approach problems with little or no idea what our results should look like. <br>
We can derive structure from data where we don't necessarily know the effect of the variables.<br>

We can derive this structure by clustering the data based on relationships among the variables in the data.<br>

With unsupervised learning there is no feedback based on the prediction results.<br>
<br>
<strong>Example:</strong><br>
<br>
Clustering: Take a collection of 1,000,000 different genes, and find a way to automatically group these genes <br>
into groups that are somehow similar or related by different variables, such as lifespan, location, roles, <br>
and so on.<br><br>

Non-clustering: The "Cocktail Party Algorithm", allows you to find structure in a chaotic environment. <br>
(i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).<br>
<hr><br>
<h3>Supervised learning Model Representation</h3><br>

<img src="https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/H6qTdZmYEeaagxL7xdFKxA_2f0f671110e8f7446bb2b5b2f75a8874_Screenshot-2016-10-23-20.14.58.png?expiry=1611792000000&hmac=cqtMQlTK9mMvVbM28xf7tYYXMG44sEC1AnpGz-eTrhk">
<br>Function h is called htpothesis.
<hr>
<h3>Cost function</h3><br>
<img src="https://user-images.githubusercontent.com/67510613/105865886-b5d3f700-6036-11eb-84e7-fb705c826a50.JPG">
<img width="415" alt="goal" src="https://user-images.githubusercontent.com/67510613/106297264-da79da00-6295-11eb-9d84-e6bc59eb2c1b.PNG">
<img width="525" alt="min" src="https://user-images.githubusercontent.com/67510613/106292445-2cb7fc80-6290-11eb-89d8-c56956e31306.PNG">
MSE같은 손실함수는 정담에 대한 오류를 숫자로 나타내는 것으로 오답이 가까울 수록 큰 값이 나오고 반대로 정답에 가까울수록 작은 값이 나온다.<br>

<hr>
<h3>Gradient decent</h3><br>
<img width="407" alt="gd" src="https://user-images.githubusercontent.com/67510613/106299400-71479600-6298-11eb-8f24-21f37a1473eb.PNG">
<br> 초기화는 일반적으로 theta1과 theta2를 모두 0으로 한다. 그리고 기울기하강법을 통해 thata1,2를 조금씩 바꾸면서 J값을 조금이라도 줄이는 것을 목표로한다.

<img width="409" alt="gd2" src="https://user-images.githubusercontent.com/67510613/106301114-a94fd880-629a-11eb-9e10-21b851626909.PNG">
<br> alpha는 훈련비율(learning rate)로 얼마나 많은 값이 변하는가에 대한 변수이다. 
<br> <strong>gradient decent 수식의 이해</strong><br>
<br>
<img width="415" alt="gd3" src="https://user-images.githubusercontent.com/67510613/106308004-74944f00-62a3-11eb-87cd-152e6ead8202.PNG">
식에서 alpha를 감소시킬 이유가 없는 이유가 무엇인가? : local min값에 가까워질수록 기울기(미분계수)는 0에 가까워지고(작아지고) 따라서 <br>
이동거리는 alpha를 fix했더라도 알아서 자연스럽게 감소한다.
<hr>
<h3>Cost function & Gradient decent</h3><br>
기울기 하강을 이용해서 cost function을 최소화시켜보자<br>
<img width="351" alt="cofunc,gd" src="https://user-images.githubusercontent.com/67510613/106310895-9ee80b80-62a7-11eb-8129-45a9af806716.PNG">
<img width="274" alt="cogd" src="https://user-images.githubusercontent.com/67510613/106311330-52510000-62a8-11eb-9f0e-7c7de18628b9.PNG">
<br>batch gradient decent? 전체 데이터셋에 대해 에러를 구하고 기울기를 한번만 계산하는 방식인거같음. 
<hr><br>
<h2>2nd week</h2><br>





