# EMBwithLLM: Improve text embeding with efficient LLM

LLM을 텍스트 임베딩 성능 개선에 도입한 연구로 비용적인 측면에서 저비용의 임베딩 모델과 작은 파라미터를 가진 LLM 모델을 사용하여 임베딩 성능을 개선함으로써 저비용으로 고효율 실현한다.

코드는 [여기](#https://github.com/EMBwithLLM/EMBwithLLM)서 확인할 수 있습니다.

논문은 [여기](#)서 확인할 수 있습니다.

## Team Member

이호영: [https://github.com/ihobbang250]
이원석: [https://github.com/leew0nseok] 
이수경: [https://github.com/sugyeong-lee] 
김예인: 
김동휘:


## Embedding Model


임베딩 모델로는 파라미터 수는 110M으로 대규모 모델보다 적은 편에 속하며, 상당히 작은 크기에도 불구하고 다양한 NPL 작업 및 코드 검색 등 다양한 도메인에서 높은 성능을 보인`gte-large` 를 사용하였습니다.

 [https://huggingface.co/thenlper/gte-large](https://huggingface.co/thenlper/gte-large)

## LLM Model


LLM모델은 사이즈가 작아 활용성이 높고 임베딩 미세조정의 성능을 떨어뜨리지 않는 합리적인 모델로 Mistral기반에서 파인튜닝 된 모델인 `Starling-RM-7B-alpha` 를 사용하였습니다.

[https://huggingface.co/berkeley-nest/Starling-RM-7B-alpha](https://huggingface.co/berkeley-nest/Starling-RM-7B-alpha)

## Datasets

데이터셋으로는 Bank77, FewNerd, StackEx, MTOP(D) 총 4가지 데이터셋을 사용했습니다.

| Task | Name | #clusters | #data(small) |
| --- | --- | --- | --- |
| Intent | Bank77 | 77 | 3,080 |
| Type | FewNerd | 58 | 3,789 |
| Topic | StackEx | 121 | 4,156 |
| Domain | MTOP(D) | 11 | 4,386 |