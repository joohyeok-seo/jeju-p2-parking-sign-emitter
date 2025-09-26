제주공항 P2 주차장 전광판 송출기 (Jeju P2 Parking Sign Emitter)

Raspberry Pi에서 주차면 상태(JSON)를 받아 ACE/BDF 그룹으로 집계하고, 각 전광판 컨트롤러로 UDP(유니캐스트) 메시지를 보내는 경량 송출기입니다. 표지 #2~#6 대상(설정으로 변경 가능). 샘플 재생/실시간 수신, 임계치·매핑 설정을 지원합니다.

Quick Start
git clone <YOUR_REPO_URL> && cd <REPO>
# (선택) 가상환경
python3 -m venv .venv && source .venv/bin/activate
python -m pip install --upgrade pip

A) 사무실 테스트(샘플 재생, UDP 미송신)

.env 설정

FROM_FILE=./jeju_parking/a_company_samples.jsonl
SEND_ENABLED=false


실행

python jeju_parking/p2_sign_emitter.py
