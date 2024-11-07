## 1. 소개 및 기획 배경
### 프로젝트 목표
이 프로젝트는 한국 화장품을 구매하려는 외국인 고객을 대상으로, 한국 인플루언서 추천 정보를 기반으로 개인화된 화장품을 추천하는 챗봇 시스템을 구축하는 것입니다. 사용자의 요구에 맞는 제품을 추천해 고객이 더 쉽고 빠르게 제품을 선택할 수 있도록 돕습니다.

### 기획 배경
이 시스템은 실제 경험을 바탕으로 기획되었습니다. 한국에 온 교환학생들에게 화장품을 추천할 때, 한국 현지인의 추천 정보가 대부분 한국어로 제공되어 접근이 어려운 문제를 경험했습니다. 또한, 외국인 고객들이 한국 화장품을 선호하는 경향이 있어, 언어 장벽을 해결할 필요성을 느꼈습니다.

따라서, 한국인 인플루언서의 추천 정보를 영어로 변환하여, 외국인 고객에게 적합한 화장품을 추천하는 시스템을 기획하였습니다. 이를 통해 외국인 관광객들이 한국 화장품을 더 쉽게 선택하고, 구매 결정을 돕는 역할을 할 것으로 기대됩니다.

## 2. System Architecture Diagram


```mermaid
graph LR
    User -->|Input Query| StreamlitUI[Streamlit UI]
    StreamlitUI -->|Invoke function| answer_by_gpt2
    answer_by_gpt2 -->|Generate prompt| OpenAIAPI[OpenAI API]
    OpenAIAPI -->|Return response| answer_by_gpt2
    answer_by_gpt2 -->|Display response| StreamlitUI
    StreamlitUI -->|Store conversation| SessionState[Session State]
    StreamlitUI -->|Display to user| User
```
## 3. 설치 및 실행 방법

<details>
  <summary>필수 요구 사항</summary>
  
  - Python 3.11
  - Poetry (패키지 관리 도구)
</details>

<details>
  <summary>Python 설치</summary>
  
  Python이 설치되어 있지 않다면, 아래 방법으로 Python 3.11을 설치해주세요:
  
  - **Windows**: pyenv 설치 가이드를 참고하여 pyenv를 통해 Python 3.11 설치
  - **Mac**: Homebrew를 통해 pyenv로 Python 3.11 설치
</details>

<details>
  <summary>Poetry 설치</summary>
  
  Poetry가 설치되어 있지 않다면, 아래 명령어로 Poetry를 설치하세요:
  
  **Windows:**
  ```
  pip install poetry
  ```
  **Mac:**
  ```
  pip3 install poetry
  ```
</details>

<details>
    <summary>프로젝트 파일 준비</summary>
프로젝트 디렉토리에서 pyproject.toml과 poetry.lock 파일을 확인하세요. 이 파일들이 있어야 필요한 패키지가 자동으로 설치됩니다.
</details>

<details>
    <summary>가상환경 설정 및 패키지 설치</summary>
프로젝트 디렉토리로 이동 후, 아래 명령어를 실행하여 가상환경을 생성하고 필요한 라이브러리를 설치하세요:
    
  ```
  poetry install
  ```
</details>

<details>
    <summary>가상환경 활성화</summary>
가상환경을 활성화하려면, 아래 명령어를 실행하세요:
    
  ```
  poetry shell
  ```
</details> 

<details>
    <summary>프로그램 실행</summary>
가상환경이 활성화된 후, 아래 명령어로 챗봇 프로그램을 실행할 수 있습니다:
    
  ```
  streamlit run main.py
  ```
</details> 

## 4. 사용법
## 5. 구성 요소 설명
## 6. 환경 변수 설정
## 7. 주요 의존성 및 기술 스택