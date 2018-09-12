# golang-mysql
## 다운받는 방법  
  ``` go get -u github.com/go-sql-driver/mysql```
## 연동 하는 방법
  ```sql.open("mysql", "root:mysql비밀번호@tcp(127.0.0.1:3306)/디비이름")```
    root 는 mysql 사용시 디폴트 값 tcp(127.0.0.1:3306) 도 디폴트 값 특별하지 않     은이상 그대로 사용 권고  
## 쓸수 있는 함수들 
  ```db.query("INSERT INTO chat_record VALUES ('')")```
    여기서 chat_record 은 table 이름 그렇므로 사용하고 있는 테이블의 이름을 쓰면    됩니다 ' ' 사이에 들어갈것은 저장하고싶은 값
  ```insert, err := db.Query("SELECT c_r FROM chat_record")
	if err != nil {
		panic(err.Error())
	}
	for insert.Next() {
		var chat chat_record
		err = insert.Scan(&chat.chat)
		if err != nil {
			panic(err.Error())
		}
		fmt.Println(chat.chat)
	}
``` 
여기서 의 scan 함수는 기존 디비에있는 값을 읽어 들이기 위해 재공되는 함수입니다.scan 함수을 읽어들이기 위해서는 미리 struct 을 만들어 struct 안에 변수들을 만들어 값을 받아와야합니.       
 
