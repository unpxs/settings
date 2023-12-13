
[Chrome](https://www.google.com/intl/ko_kr/chrome/)

## PowerShell 실행 정책
`RemoteSigned` 로컬 스크립트 제한 없이 실행가능, 인터넷에서 다운로드한 스크립트는 디지털 서명 필요.
```
Set-ExecutionPolicy RemoteSigned
```

## choco
### choco 파워쉘 설치
```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
### 패키지 검색: `choco list`
```
choco install vim brave vscode honeyview bandizip authy-desktop -y
choco install autohotkey --version=1.1.37.01

choco install nodejs python curl -y
choco install github-desktop -y
choco install git -y

choco install yt-dlp telegram tabby vlc ffmpeg logseq copyq obsidian pandoc chromium -y
```


## winget
- FastStone Capture설치
	```
	winget install FastStone.Capture
	```
- 업그레이드
	```
	winget upgrade FastStone.Capture
	```

## schtasks
`schtasks`등록 
### AHK
- Alt_mouse
	```
	schtasks /Create /SC ONLOGON /TN "Alt_mouse" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\FIXED\Alt_mouse.ahk'" /RL HIGHEST
	```
- en-ko-conv
	```
	schtasks /Create /SC ONLOGON /TN "en-ko-conv" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\FIXED\en-ko-conv.ahk'" /RL HIGHEST
	```
- leftrightupdown
	```
	schtasks /Create /SC ONLOGON /TN "leftrightupdown" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\FIXED\leftrightupdown.ahk'" /RL HIGHEST
	```
- Spacedesk
	```
	schtasks /Create /SC ONLOGON /TN "Spacedesk" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\FIXED\Spacedesk.ahk'" /RL HIGHEST
	```
- doublekeyinput
	```
	schtasks /Create /SC ONLOGON /TN "doublekeyinput" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\FIXED\doublekeyinput.ahk'" /RL HIGHEST
	```
### Sizer
```
schtasks /create /tn "Sizer 실행" /tr "%USERPROFILE%\Documents\Sizer\sizer.exe" /sc ONLOGON /rl HIGHEST
```

### Python `watchdog`
스크립트 시작 프로그램 자동 등록 (관리자 권한 실행)
```
schtasks /Create /SC ONLOGON /TN "pyStart" /TR "'C:\Program Files\AutoHotkey\AutoHotkey.exe' '%USERPROFILE%\ahk\pyStart.ahk'" /RL HIGHEST
```

## 개별 설치
- UpNote: [install 7.6.2.0v](https://api.onedrive.com/v1.0/shares/u!aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBb29CcEhsY1dHZi1rY0VVS1RaOEQxX2dKZ3NRenc_ZT1YRmdtTko/root/content)
- https://todoist.com/ko/downloads/windows
- https://wrtn.ai/
- https://cursor.sh/
- https://caret.io/
- https://www.deepl.com/ko/app/
- https://www.figma.com/
- [min](https://minbrowser.org/): [install 1.30.0v](https://api.onedrive.com/v1.0/shares/u!aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBb29CcEhsY1dHZi1sSmN2Sk5VTGFFTEI4VG9vWkE_ZT1MbjV4Yks/root/content)
	- 실시간 보호 해제
- https://www.canva.com/download/windows/
- https://sparkmailapp.com/download

## 드라이버
인튜어스 드라이버: DTK-1301 [링크](https://www.wacom.com/ko-kr/support/product-support/drivers)

## Python
```
python -m pip install --upgrade pip

# pip list

pip3 install pyperclip
pip3 install boto3 clipboard pillow win10toast pywin32
pip3 install regex requests mistune
pip install plyer b2sdk pynput regex watchdog

pip install pandas tabulate 

# Google Sheet API 
pip install oauth2client gspread
pip install google-api-python-client

pip install cloudinary==1.26.0
pip install pyautogui 
```


## `.myConfig`
```
#userprofile%/.aws
├─credentials
└─config
```


## node.js
```
npm install


cd "%userProfile%\script\node_script\gui_text_editor"
npx electron .
```


## NerdFonts
https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/Hack.zip


## Mountain Duck
- 설치: https://mountainduck.io/


## Win + L OFF
[.reg Download](https://dl.1tz.in/2023/12/win_L_Lock.reg)
