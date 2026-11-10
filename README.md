# Seizia Rust CLI 다운로드

GitHub 계정 없이 테스트 버전 `v0.1.0-test.1`을 설치할 수 있습니다. 설치에 Rust, Node.js, GitHub CLI가 필요하지 않습니다. [실행 파일과 체크섬](https://github.com/froiibn/seizia-rust-downloads/releases/tag/v0.1.0-test.1)

## Windows x64

PowerShell에 붙여넣으세요.

```powershell
$installer = Join-Path $env:TEMP 'install-seizia.ps1'
Invoke-WebRequest -UseBasicParsing -ErrorAction Stop -Uri 'https://github.com/froiibn/seizia-rust-downloads/releases/download/v0.1.0-test.1/install-seizia.ps1' -OutFile $installer
powershell -NoProfile -ExecutionPolicy Bypass -File $installer
```

설치 후 새 터미널에서 `seizia`를 실행하세요.

## macOS와 Linux

macOS는 Apple Silicon과 Intel을, Linux는 x64를 지원합니다.

```sh
installer="$(mktemp)"
curl -q -fLsS 'https://github.com/froiibn/seizia-rust-downloads/releases/download/v0.1.0-test.1/install-seizia.sh' -o "$installer" &&
  sh "$installer" &&
  export PATH="$HOME/.local/bin:$PATH" &&
  seizia --version
rm -f "$installer"
```

`seizia`를 실행하세요. 이후 터미널에서도 명령을 쓰려면 `~/.local/bin`이 셸의 `PATH`에 있어야 합니다.
