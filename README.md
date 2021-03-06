# Natural-Language-Inference
자연어의 이해와 추론


# Entailment    

## 데이터 생성시 고려할 점         

### Between-item variability     
술어의 원형(predicate lemma) 외에도 시제, 인칭 등이 영향을 미칠 것으로 보인다. 또한 영어에서는 finite clausal complements 에 대한 논의가 있었고 국어에서는 보문소(('-것, -다고/-라고, -음/-기))의 영향에 대한 논의가 있었다.(Marneffe(2019), (Lee, C. and D. Chung(2018)등 참조)    

- 영어    
(예)Jane knows that it is snowing. - it is snowing. 

- 국어    
(예) 제인은 눈이 온 것을 안다.   또는 제인이 눈이 왔다고 안다.  


### Between-annotator variability     
같은 문장이라도 판단하는 사람에 따라 확신성의 정도(degree)가 달리질 수 있다. (Marneffe(2019에서 주로 논의됨)                        

# 관련 논문과 코드

|번호|논문| PDF| CODE |
|:---:|:-----------------:|:-----------------:|:-----------------:|
|1|anjiang Jiang and Marie-Catherine de Marneffe. 2019. "Evaluating BERT for natural language inference: a case study on the CommitmentBank." In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing (EMNLP 2019). |[논문 링크](https://www.aclweb.org/anthology/D19-1630.pdf)|https://github.com/nyu-mll/jiant|
|2|Nanjiang Jiang and Marie-Catherine de Marneffe. 2019. "Do you know that Florence is packed with visitors? Evaluating state-of-the-art models of speaker commitment." In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (ACL 2019). Best short paper award.| [논문 링크](https://www.aclweb.org/anthology/P19-1412/)|-|
|3|Marie-Catherine de Marneffe, Mandy Simons and Judith Tonhauser. 2019. "The CommitmentBank: Investigating projection in naturally occurring discourse." In Proceedings of Sinn und Bedeutung 23. |[논문링크](https://semanticsarchive.net/Archive/Tg3ZGI2M/Marneffe.pdf)|https://github.com/mcdm/CommitmentBank|


# 데이터

## 영어    
- 영어 데이터 [링크](https://aclweb.org/aclwiki/Textual_Entailment_Resource_Pool)   
- GLUE 데이터 [링크](https://super.gluebenchmark.com/tasks/)
- 관련 논문 [링크](https://w4ngatang.github.io/static/papers/superglue.pdf) : Wall Street Journal, British National Corpus의 소설, Switchboard에서 추출됨

(논문 5쪽) 확신성의 정도에서 0 인 예시

B: And yet, uh, I we-, I hope to see employer based, you know, helping out. You know, child, uh,care centers at the place of employment and things like that, that will help out. 
   
A: Uh-huh.     
    
B: What do you think, do you think we are, setting a trend?                   
     
Hypothesis: they are setting a trend       
Entailment: Unknown         
      

 
## 국어:kakaobrain_KorNLUDatasets                 
- 데이터 링크 : https://github.com/kakaobrain/KorNLUDatasets           
    
- 관련 논문: https://arxiv.org/abs/2004.03289       

- 허깅페이스 페이지 (왼쪽 Dataset에서 kor_nli)에도 들어 있다.  [링크](https://huggingface.co/nlp/viewer/?fbclid=IwAR3gXfTsvaWKj1zW_b00SDsBTKmbudiMOeJQeuRmU8BX5s4c8B9v4Lqe6T4)   

- pip install nlp 로 쓸 수 있다고 한다.        

   

 ## 언어 추론에서 데이터 세트의 방향성             

- 다양한 문장 길이와 문장 형태를 반영한 데이터 세트도 필요하다.            
- 대규모 데이터 세트 뿐만 아니라 정교하게 구축되어 확장성이 좋은 데이터 세트도 필요하다.(이 글을 쓴 이유)       

데이터의 확장성은 몇 가지 방향에서 이루어질 수 있는데 먼저, Entailment는 Neutral-Contradiction 데이터와 함께 구축되어 세트처럼 분석되어 왔다. 이 외에도. Superglue에는 자연어 이해를 위한 다양한 데이터(https://super.gluebenchmark.com/tasks/ )가 들어 있다.          

![Superglue](./superglue.png)              



또 따른 방향으로는  Semantic textual similarity (STS)와도 깊은 관련성이 있다. 카카오브레인의 KorSTS와 조원익님의 https://github.com/warnikchow/paraKQC 데이터를 참고할 수 있다.           



 ## 어디에 쓸까?

 Anjiang Jiang 은 강연(https://vimeo.com/385255521)에서 truthteller에 대해 언급한 적이 있다. 데이터가 공개적으로 구축되는 경우. 에는 이러한 응용도 고려해 만하다고 생각된다. 하지만 영어에서 truthteller가 아직 안 나오고 있는 것을 통해 어떤 사실에 대해 확신(commitment)의 정도를 측정하는 것이 쉽지 않음을 알 수 있다.                              


![truthteller](./teller.png)


## Commitment Bank 외에 Bank 형태의 코퍼스들       
                    
-Penn Discourse TreeBank (Miltsakaki et al. 2004) [링크](https://catalog.ldc.upenn.edu/LDC2008T05),       
-TimeBank(Pustejovsky et al. 2006), [링크](https://catalog.ldc.upenn.edu/LDC2006T08)     

        
  

 
