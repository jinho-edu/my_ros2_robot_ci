# 베이스 이미지: 공식 ROS 2 Humble 이미지 사용
FROM ros:humble-ros-base-jammy

# ROS 2 파이썬 패키지 빌드에 필요한 도구 설치
# pip 설치, colcon 빌드 도구 설치
RUN apt-get update && apt-get install -y \
    python3-pip \
    python3-colcon-common-extensions \
    git \
    --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*

# 작업 디렉토리 설정
WORKDIR /ros2_ws

# ROS 2 워크스페이스에 소스 코드를 복사할 임시 디렉토리 생성
# .github/workflows의 ci.yml에서 이 디렉토리로 소스코드를 복사합니다.

# 엔트리포인트 스크립트를 사용하여 ROS 환경 설정
# CMD ["/bin/bash"]