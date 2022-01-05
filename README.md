# Jira 와 JQL 사용법

- Issue Tracking (Project Management)
- Agile, DevOps, SRE

#### JQL

- Jira Query Language
- Jira Issue 구조적 검색을 위한 언어
- SQL 과 비슷한 문법
-  Jira의 각 필드들에 맞는 특수한 예약어 제공
- 쌓인 Issue들을 재가공해 유의미한 데이터를 도출해 내는데 활용

```
=, !=, >=, >
in, not in
~(contains), !~ (not contains)
is empty, is not empty, is null, is not null
AND
OR
NOT 
EMPTY
NULL
ORDER BY 
```

```
endOfDay(), startOfDay()
endOfWeek()(Saturday), startOfWeek()(Sunday)
endOfMoneth(), startOfMonth(), endOfYear(), startOfYear()
currentLogin()
currentUser()
```

```
project = DP AND updated > startOfWeek()
project = DP and assignee = sangjinsu
project = DP AND updated > startOfWeek(1d) and updated < endOfWeek(-1d)
project = DP AND assignee = currentUser() and resolution = Unresolved
```

