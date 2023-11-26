### MySQL 서버 내 실행 중인 쓰레드 목록 조회
```
SELECT thread_id, name, type, processlist_user, processlist_host FROM performance_schema.threads ORDER BY type, thread_id;
```

### R/W Background 쓰레드 수 지정
- innodb_write_io_threads
- innodb_read_io_threads

### 엔진 확인
```
SHOW ENGINES;

YES: 스토리지 엔진이 포함되어 있고 사용 가능으로 활성화
DEFAULT: YES와 동일한 상태이지만 필수 스토리지 엔진임을 의미
NO: 현재 서버에 포함되지 않았음을 의미
DISABLED: 서버에는 포함되었지만, 파라미터에 의해 비활성화된 상태
```

### 플러그인 확인
```
SHOW PLUGINS;
```

### 컴포넌트 관련
```
INSTALL COMPONENT '...'

SELECT * FROM mysql.component;
```

### 외래키 체크 해제
foreign key check를 OFF