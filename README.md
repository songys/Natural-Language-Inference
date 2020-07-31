# Natural-Language-Inference
자연어의 이해와 추론


## 화자(speaker)/필자(writer)의 확신 정도

- 영어    
(예)Jane knows that it is snowing.        

- 국어    
(예) 제인은 눈이 온 것을 안다.   또는 제인이 눈이 왔다고 안다.     
                   
위의 예와 같이 국어는 보문소('-것, -다고/-라고, -음/-기)와 술어의 결합으로 화자(speaker)/필자(writer)의 확신 정도를 나타낸다.  

## 데이터 생성시 고려할 점

- Between-item variability
술어의 원형(predicate lemma) 외에도 시제, 인칭 등이 영향을 미칠 것으로 보인다. 또한 영어에서는 finite clausal complements 에 대한 논의가 있었고 국어에서는 보문자의 영향에 대한 논의가 있었다.(Marneffe(2019), (Lee, C. and D. Chung(2018)등 참조)    


- Between-annotator variability 
같은 문장이라도 판단하는 사람에 따라 확신성의 정도(degree)가 달리질 수 있다.   

# 관련 논문과 코드

|번호|논문| PDF| CODE |
|:---:|:-----------------:|:-----------------:|:-----------------:|
|1|anjiang Jiang and Marie-Catherine de Marneffe. 2019. "Evaluating BERT for natural language inference: a case study on the CommitmentBank." In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing (EMNLP 2019). |[논문 링크](https://www.aclweb.org/anthology/D19-1630.pdf)|-|
|2|Nanjiang Jiang and Marie-Catherine de Marneffe. 2019. "Do you know that Florence is packed with visitors? Evaluating state-of-the-art models of speaker commitment." In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (ACL 2019). Best short paper award.| [논문 링크](https://www.aclweb.org/anthology/P19-1412/)|-|
|3|Marie-Catherine de Marneffe, Mandy Simons and Judith Tonhauser. 2019. "The CommitmentBank: Investigating projection in naturally occurring discourse." In Proceedings of Sinn und Bedeutung 23. |[논문링크](https://semanticsarchive.net/Archive/Tg3ZGI2M/Marneffe.pdf)|https://github.com/songys/CommitmentBank|



# GLUE 
관련 논문 : https://w4ngatang.github.io/static/papers/superglue.pdf

(논문 5쪽) 확신성의 정도에서 0 인 예시

B: And yet, uh, I we-, I hope to see employer based, you know, helping out. You know, child, uh,care centers at the place of employment and things like that, that will help out. 
   
A: Uh-huh.     
    
B: What do you think, do you think we are, setting a trend?                   
     
Hypothesis: they are setting a trend       
Entailment: Unknown         
   

데이터 : https://super.gluebenchmark.com/tasks/    

 -대상 코퍼스 : Wall Street Journal, British National Corpus의 소설, Switchboard     



## Commitment Bank 외에 Bank 형태의 코퍼스들    
                    
-Penn Discourse TreeBank (Miltsakaki et al. 2004) [링크](https://catalog.ldc.upenn.edu/LDC2008T05),       
-TimeBank(Pustejovsky et al. 2006), [링크](https://catalog.ldc.upenn.edu/LDC2006T08)                



















