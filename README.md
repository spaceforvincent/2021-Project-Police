# <선제적 치안대책 수립을 위한 치안지도 서비스>



## 1. 기획 배경 및 목적

창원시는 인구 100만 이상의 도시로 특례시로의 승격을 앞두고 있는 상황이다 (2021년 기준). 이를 기점으로 치안 분야에서 자치경찰과 함께 지역 맞춤형 치안서비스 제공을 목표로 하고 있다. 우리나라는 2021년 7월부터 전국적으로 자치경찰제를 시행하고 있지만 제도적으로 책임 소재가 불분명하다는 점, 치안 데이터는 지방으로 내려갈수록 데이터가 적어져 개인을 특정하는 경우 등의 문제가 발생할 수 있다는 점에서 경찰 측에서 공무원 측에 데이터를 제공하는 것을 꺼리고 있다.

그래서 공무원들을 대신하여 데이터를 통합하고 표기하여 그것을 기반으로 예측까지 수행하는 서비스를 제시한다. 서비스의 궁극적인 목적은 실시간 모니터링을 통한 즉각적인 대응과 협업을 가능하게 하고, 데이터를 근거한 선제적 정책 수립을 지원하는 것이다.



## 2. 활용 데이터

경찰대학 치안정책연구소 - 신고접수 위치데이터(종속변수 활용)

SK텔레콤 - 유동인구 데이터(독립변수 활용, 치안정책 연구소에서 지원)

그 외 스마트 치안 빅데이터 플랫폼, 창원시 빅데이터 포털, 공공데이터 등에서 인구, 공간, 지역데이터 등을 수집해서 독립변수로 사용하였고 일부 시각화 하였다.





## 3. 단계별 기획

기능과 웹페이지 구성에 있어서 크게 3단계로 나눠서 진행하였다. 1단계는 경남 내의 창원 지도, 2단계는 창원 내 5개 구 지도, 마지막으로 3단계는 구를 100 x 100으로 나눠서 예측까지 하는 지도이다.



1단계에서는 산재된 데이터를 통합하여 병렬적으로 표시해주는 지도 서비스를 구축하고자 하였다. 치안데이터의 경우에는 데이터 대부분이 경찰서 관할구역 단위로 표기가 되어있기 때문에 이런 것을 어떻게 행정동과 매칭할 수 있을까 하는 문제점이 있었는데, 다행히 창원시의 경우에는 행정동 경계와 경찰서 관할 경계가 유사했기 때문에 일부 매칭을 시켜서 행정동 별로 표기할 수 있었다.



앞에서는 정형화된 데이터를 수집해서 병렬적으로 나열했다면 2단계 지도에서는 비정형 데이터를 수집해서 표기를 하고, 정형데이터는 증감을 비교해서 해당 수치를 보기 편하도록 시각화하여 제공한다. 지역 맞춤형 지도를 제작할 시에 특히 중요한 것은  지역 주민들이  관심이 있어 하는 것을 보여주는 것이라고 생각했는데, 그런 데이터를 구하고 선정하기가 쉽지 않았다. 있다고 하더라도 대부분 경찰서에서 경찰서 방문객을 대상으로만 수집을 하다보니 정확도가 떨어진다는 문제가 있었다. 따라서 뉴스데이터를 크롤링해서 지역에서 어떤 뉴스가 자주 나오는지를 파악하여 어떤 문제에 대해서 관심을 가져야 좋은가에 관한 키워드를 추출해서 제공하려고 하였다.



3단계에서는 100x100으로 격자분석을 진행하였다. 기존에 진행한 동 단위 분석을 할 필요가 없기 때문에 작은 단위 분석을 진행할 수 있고, cctv나 가로등 개수가 지역범죄에 미치는 영향력과 같은 공간적 분석도 할 수 있으며, 격자마다 다르게 나오는 결과를 가지고 범죄 유형등급을 예측하고, 예측된 유형등급을 통해 정책 수립에 도움이 되도록 하였다.

실제 발생 지역과 예측이 유사하긴 하지만 예측 결과가 좀 더 퍼져있는 것을 볼 수 있다. 범죄가 아직 일어나지 않은, 범죄 발생 가능성이 있는 지역은 잘 예측하지만 범죄가 일어났을 때 얼마나 일어났는가를 예측하는 데는 정확도가 떨어진다고 할 수 있다. 하지만 구별로 다시 나눠서 진행하면은 조금 더 자세히 나온다는 것을 볼 수 있다. 5개년으로 데이터를 늘릴 시 조금 더 정확해질것으로 예상한다.

예측도 중요하지만 더 중요하게 본 것은, 대책을 세울 때 지역에서 어떤 변수가 중요한가 하는 것이다. 다양한 알고리즘에 다양한 변수 중요도를 제공을 해서 공통적으로 나오는 부분이 유용하지 않을까 싶어서 함께 제공하였다.



## 4. 기대효과

1단계 지도를 통해서 산재되어있는 데이터를 한 데 모음으로써 데이터 수집에 소비되는 시간 및 경제적 비용 감소효과를 누릴 수 있게 되고, 공시 의무 중 하나인 지역 안전지수를 경남 내 다른 지역과 쉽게 비교할 수 있게 된다.

2단계 지도를 통해서는 주요 키워드를 실시간으로 모니터링하여 대응을 강화할 수 있게 된다.

3단계 지도에서는 공간분석 뿐만 아니라 기후 시간대 분석까지 추가로 진행한다면 조금 더 데이터 기반의 행정을 구축할 수 있을 것이다.

<개선이 필요한 사항>

1. 사이트에서 크롤링을 하다보면 같은 뉴스가 다른 표현으로 나오는 경우가 있다.

ex) 절도가 일어났다 = 도난 당했다.

그런 사항들은 어떻게 구분을 할 것인가에 대한 이슈는 해결하지 못했다.

2. 뉴스 사이트 측에서 크롤링을 막아 놓았을 때의 대안도 마땅히 없었다.

<느낀 점>

아무래도 민감한 데이터다 보니 경찰대학 측에서 제공받은 데이터 이외에 팀원 모두가 데이터를 모으는데 고생을 좀 했던 것 같다. 크롤링을 이용하거나 수집 가능한 범위내에서 수집을 진행했다. 이번 프로젝트에서는 공간 분석을 통한 예측을 보여줬는데, 사실 공간하고 상호 관계가 있는 범죄가 있고 그렇지 않은 범죄가 있을 수 있다. 공간 관련성이 있는 경우는 CPTED(**C**rime **P**revention **T**hrough **E**nvironmental **D**esign : **환경 설계를 통한 범죄 예방)**과 같은 기법들을 적용할 수 있지만 그 외의 것은 캠페인 등과 같은 다른 방법으로 예방을 해야 한다. 그런 고려 가능한 범위까지도 포함을 해서 조금 더 서비스 활용방법론들을 제시 했으면 더 좋았을 것 같다.

원래는 경찰을 대상으로 제공하려던 서비스였으나, 이미 경찰들은 PRE-CAS라고 하는 이미 사용 중인 서비스가 있었다. 노인이나 시민들에게 제공하는 형태도 생각을 했지만 그렇게 했을 때 범죄에 악용될 우려나 불편을 초래할 우려가 있어 대상을 공무원으로 정하게 된 것 같다. 이미 구상되어 있는 서비스가 많아서 기획이 참 어렵다는 것을 느끼게 되었다.



