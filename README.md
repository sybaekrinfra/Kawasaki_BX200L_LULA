# Kawasaki BX200L LULA Test Widget 설정 파일

NVIDIA Isaac Sim의 **LULA Test Widget**에서 Kawasaki BX200L 로봇을 테스트하기 위한
URDF 및 Robot Descriptor 설정 파일입니다.

## 지원 버전

- Isaac Sim 5.0.0 ~ 6.0.1

## 파일 구성

| 파일 | 설명 |
| --- | --- |
| `BX200L_C001.urdf` | BX200L의 링크 및 6축 관절 정보를 정의한 URDF |
| `BX200L_C001_robot_descriptor.yaml` | LULA의 관절 공간, 관절 제한 및 충돌 구체를 정의한 Robot Descriptor |

## 사용 방법

1. Isaac Sim을 실행합니다.
2. LULA Test Widget을 엽니다.
3. Robot Description 파일로
   `BX200L_C001_robot_descriptor.yaml`을 선택합니다.
4. URDF 파일로 `BX200L_C001.urdf`를 선택합니다.
5. 설정을 로드한 후 관절 동작, 충돌 구체 및 모션 생성 결과를 확인합니다.

파일을 이동하거나 복사할 때는 두 파일을 함께 관리하는 것을 권장합니다.

## 주요 설정

- 관절: `joint1` ~ `joint6`
- Root link: `link0`
- 기본 관절 자세: `[0, 0, 0, 0, 0, 0]`
- Robot Descriptor 기준 End-effector frame: `link6`
- 관절 단위: radian
- 길이 단위: meter

## 참고 사항

- 이 저장소의 URDF는 `meshes/*.obj` 경로를 참조하지만 메시 파일은 포함하지 않습니다.
  따라서 로봇의 시각 및 메시 기반 충돌 형상을 표시하려면 해당 경로에 별도의 메시
  파일이 필요합니다.
- Robot Descriptor에는 LULA 충돌 검사에 사용할 링크별 collision sphere가
  정의되어 있습니다.
- 실제 장비에 적용하기 전에는 로봇 사양, 관절 제한, 속도 및 가속도 제한을 반드시
  확인하십시오.

## 라이선스

이 저장소에 포함된 `BX200L_C001.urdf`와
`BX200L_C001_robot_descriptor.yaml`은 [MIT License](LICENSE)에 따라
사용할 수 있습니다.

- 제작자: SooYoun Bae
- 소속: KRINFRA (주식회사 한국인프라,
  Infra Information Technology Co., Ltd.)

URDF에서 참조하는 `meshes/*.obj` 파일은 이 저장소에 포함되어 있지 않으며,
이 저장소의 MIT License 적용 대상이 아닙니다. 메시 파일을 별도로 사용하는 경우
해당 파일의 라이선스와 재배포 조건을 확인하십시오.

Kawasaki 및 BX200L은 각 권리자의 상표 또는 제품명입니다. 이 프로젝트는
Kawasaki Robotics의 공식 프로젝트가 아니며, Kawasaki Robotics가 보증하거나
후원하지 않습니다.
