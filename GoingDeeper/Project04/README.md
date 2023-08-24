# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 최지수
- 리뷰어 : 조준규


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [X] 주석을 보고 작성자의 코드가 이해되었나요?
  > 각 코드블록 별로 함수가 어떤 역할을 위해 구현된 것인지 key word를 명시해주어서 이해하기 쉬웠다.
- [X] 코드가 에러를 유발할 가능성이 없나요?
  > 전체적으로 에러를 유발할 수 있는 부분은 발견하지 못했다.
- [X] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 함수가 제대로 작동하는지 확인하는 절차가 여러 군데 있는 것으로 보아 코드를 제대로 이해했다고 생각했다.
- [X] 코드가 간결한가요?
  > 함수를 적극적으로 활용하여 반복되는 코드가 없도록 코드 길이를 최소화 하였다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 코드 이해도 예시
# height에 대해서 tensorflow가 제공하는 data의 형태를 분석하고자 함.
visualize_reverse_bbox(img,objects['bbox'].numpy()) # height 기준으로 y좌표를 빼지 않은 경우의 bbox
visualize_bbox(img,objects['bbox'].numpy()) # height 기준으로 y좌표를 뺀 경우의 bbox
```
```python
# 코드 간결성 예시
# Go, Stop 이미지에 대한 결과를 함수 하나로 잘 구현할 수 있도록 하였다.
def self_drive_assist(img_path, size_limit=300, view = False):
    result = 'Go'
    img =  cv2.cvtColor(cv2.imread(img_path), cv2.COLOR_BGR2RGB)

    ...

    return result
```

# 참고 링크 및 코드 개선
```python
# test dataset에 대해서도 Go, Stop을 잘 prediction 하는지 확인해보는 것도 좋을 것 같습니다.
# Cyclist의 경우에 사람으로 인식하는 것이 맞을지, 이에 대해서는 어떻게 처리할 지 고민해보면 좋을 것 같습니다.😁
