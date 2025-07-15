# Windowcalculation

프로젝트 개요
목표: Windows 11 기본 계산기와 동일한 디자인 및 기본 사칙연산 기능을 C# / WPF / MVVM 패턴으로 구현

패턴: MVVM (Model-View-ViewModel)

언어 / 기술: C#, .NET Framework 4.8, WPF

주요 포인트

WPF MVVM 구조 설계

RelayCommand / Command 패턴

Binding, DataContext 

숫자 입력/계산 로직

키보드 입력 처리

복사/붙여넣기 지원

숫자 3자리마다 콤마(,) 포맷 처리

최대 16자리 제한 처리

프로젝트 구조

CalculatorMVVM
├─ Model
│  └─ Calculator.cs
├─ View
│  ├─ MainWindow.xaml
│  └─ MainWindow.xaml.cs (partial class)
├─ ViewModel
│  └─ MainViewModel.cs
├─ Command
│  └─ RelayCommand.cs
└─ App.xaml

주요 기능
*사칙연산 ( +, -, , / )

키보드 입력 지원 (0~9, Backspace, Enter 등)

복사/붙여넣기 지원 (Ctrl+C, Ctrl+V)

16자리 제한 / 소수점 입력 / 쉼표(,) 표시

계산기 전용 키 입력 변환 처리

SubDisplay / MainDisplay 분리 출력

= 이후 새로운 수 입력 시 초기화 로직 적용

0으로 나누기 예외 처리

사용 기술 상세
WPF UniformGrid: 버튼 4x6 배치, 균일한 크기 유지

TextBox + ViewBox 조합: 입력값 폰트 크기 자동 조정

Binding: View ↔ ViewModel 연결 (TwoWay)

RelayCommand: Command 패턴으로 MVVM 준수

KeyEvent: 키보드 입력 → ViewModel로 전달

Clipboard API: 복사 / 붙여넣기 구현

String 기반 포맷 처리: double 사용 없이 쉼표(,) 수동 관리

파일 설명

Calculator.cs	계산 로직 처리 (Model)
MainViewModel.cs	사용자 입력, 상태 관리 (ViewModel)
RelayCommand.cs	Command 구현
MainWindow.xaml	UI View
MainWindow.xaml.cs	이벤트-ViewModel 연결 (partial class)

<img width="318" height="498" alt="image" src="https://github.com/user-attachments/assets/f5aca66b-3e06-4116-b4e7-834e2ba17513" />
<img width="317" height="497" alt="image" src="https://github.com/user-attachments/assets/d83fc5c3-07a5-487d-9e3e-93ef5e597804" />
