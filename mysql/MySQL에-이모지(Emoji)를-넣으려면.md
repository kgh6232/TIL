# MySQL에 이모지(Emoji)를 넣으려면?⛱

> 😍😨👕👑👠🍔🌽⚽️ < 이것이 이모지(Emoji)

## 에러 

MySQL 데이터베이스의 인코딩이 `uft8`일 때 이모지(Emoji)를 INSERT하면 에러가 난다.  

그 이유는 MySQL에서 `uft8` 인코딩의 한글자 당 가변 3Byte까지만 지원하는데 반해 이모지는 4Byte를 사용하기 때문. 

## 해결책

이를 해결하기 위해서는 `utf8` 대신 `utf8mb4`를 사용하면 된다. `utf8mb4`은 기존 `uft8`의 확장 버전의 캐릭터셋으로 글자당 가변 4Byte까지 지원한다.

(MYSQL 5.5.3 이후부터 선택 가능)



