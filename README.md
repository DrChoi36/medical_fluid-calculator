# 💧 소아 유지 수액 계산기 (Pediatric Fluid Calculator)

> **"Calculated Care for Little Ones"** > 진료 현장에서 소아 환자의 유지 수액 용량을 신속하게 계산하기 위해 제작된 웹 기반 계산기입니다.

## 📋 개요 (Overview)

이 프로젝트는 **Dr. Choi**가 개발한 간단한 웹 애플리케이션으로, 환아의 **나이**와 **체중**을 입력하면 하루에 필요한 총 수액량, 시간당 주입 속도(gtt/hr 아님, mL/hr), 그리고 연령별 권장 수액 종류를 즉시 계산하여 보여줍니다.

## ✨ 주요 기능 (Features)

* **유지 수액량 계산:** Holliday-Segar 공식을 기반으로 하루 총량(mL/day)과 시간당 속도(mL/hr)를 계산합니다.
* **권장 수액 제안:** 환자의 나이에 따라 적절한 수액 종류(Dextrose/Saline 비율)를 추천합니다.
* **최대 용량 제한:** 과수화 방지를 위해 하루 최대 수액량을 2,400mL로 제한하는 안전 로직이 포함되어 있습니다.
* **반응형 디자인:** PC와 모바일 환경 모두에서 직관적으로 사용할 수 있는 심플한 UI를 제공합니다.

## 🧮 계산 로직 (Medical Logic)

이 계산기는 소아과 영역에서 표준적으로 사용되는 **Holliday-Segar Method (4-2-1 Rule)**를 따릅니다.

### 1. 수액 용량 (Fluid Volume)
| 체중 (Weight) | 하루 필요량 (Daily Requirement) |
|---|---|
| **0 ~ 10 kg** | 100 mL/kg |
| **10 ~ 20 kg** | 1,000 mL + 50 mL/kg (체중 - 10kg) |
| **> 20 kg** | 1,500 mL + 20 mL/kg (체중 - 20kg) <br> *(Max limit: 2,400 mL/day)* |

### 2. 권장 수액 종류 (Fluid Type)
환자의 나이를 기준으로 전해질 및 포도당 요구량을 고려하여 제안합니다.
* **< 1세:** D5 1/4NS + 20mEq/L KCl
* **1세 ~ 8세:** D5 1/3NS 또는 D5 1/2NS + 20mEq/L KCl
* **> 8세:** D5 1/2NS + 20mEq/L KCl

---

## 🚀 사용 방법 (How to Use)

1.  이 저장소를 클론(Clone)하거나 `fluid_calculator.html` 파일을 다운로드합니다.
2.  `fluid_calculator.html` 파일을 웹 브라우저(Chrome, Safari, Edge 등)로 엽니다.
3.  환자의 **나이(세)**와 **체중(kg)**을 입력합니다.
4.  **'계산하기'** 버튼을 누릅니다.
5.  하단 결과창에서 계산된 수치를 확인합니다.

---

## 🛠️ 기술 스택 (Tech Stack)

* **HTML5:** 구조 및 입력 폼 구현
* **CSS3:** 사용자 인터페이스(UI) 스타일링
* **JavaScript (ES6):** 수액 용량 계산 알고리즘 및 DOM 조작

---

## ⚠️ 면책 조항 (Medical Disclaimer)

**본 프로그램은 진료 보조 및 교육 목적으로 제작되었으며, 전문적인 의학적 판단을 대체할 수 없습니다.**

* 탈수 정도, 전해질 불균형, 심장/신장 질환 여부 등 환자의 개별적인 임상 상태에 따라 실제 필요한 수액 요법은 달라질 수 있습니다.
* 개발자는 이 프로그램의 결과값 사용으로 인해 발생하는 어떠한 임상적 결과에 대해서도 책임을 지지 않습니다.
* 모든 처방은 반드시 담당 의사의 최종 판단하에 이루어져야 합니다.

---

## 👨‍⚕️ Author

**Dr. Dr. Choi**
* GitHub: [DrChoi36](https://github.com/DrChoi36)

<p align="center">
  &copy; 2025 Dr. Choi. All rights reserved.
</p>
