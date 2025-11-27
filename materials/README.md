# materials 폴더 안내

이 폴더는 각 주차의 PDF, 슬라이드, 강의노트 등 강의 자료를 저장하는 곳입니다.

파일명 규칙 (권장)
- `week-03.pdf`, `week-04.pdf` 처럼 `week-XX.pdf` 형식을 사용하세요.
- 파일명에 공백을 쓰지 마세요. 소문자와 하이픈(`-`) 사용을 권장합니다.

업로드 방법 (로컬에서 Git 사용)
1. `materials/` 폴더에 PDF 파일을 복사합니다.
2. Git에 추가/커밋/푸시:

```bash
git add materials/week-03.pdf materials/week-04.pdf
git commit -m "Add week 03 and week 04 lecture PDFs"
git push origin main
```

참고(파일 크기 제한)
- GitHub의 파일 업로드 제한은 일반적으로 100MB입니다. 100MB를 초과하는 파일은 커밋이 실패합니다.
- 큰 파일(예: 각 PDF가 100MB 이상)인 경우 `git lfs` 사용을 권장합니다.

Git LFS 간단 설치 및 사용 예시:

```bash
# 설치 (한번만)
sudo apt update && sudo apt install git-lfs
git lfs install

# 파일 추적 설정
git lfs track "*.pdf"

# 이후에 add/commit/push
git add .gitattributes materials/week-03.pdf
git commit -m "Add large pdfs via Git LFS"
git push origin main
```

대안
- Google Drive/Notion/클라우드 스토리지에 올리고 공유 링크를 `README.md`에 붙여넣는 방법도 있습니다.
- 학내 LMS나 파일 저장소(예: Moodle, Blackboard)를 사용할 수도 있습니다.

문제가 있거나 제가 대신 `materials/week-03.pdf` 자리표시 파일(빈 더미) 혹은 실제 파일 업로드를 만들어 드리길 원하시면 알려주세요.