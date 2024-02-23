# Local Mysql
- 로컬에서 mysql 을 쓸 수 있게 해주는 docker-compose 설정

## DB Connect

```bash
cd mysql
docker-compose up -d

# http://localhost:8082/?server=mysql%3A3306

#
# Adminer Login Info
#
# Server : mysql:3306
# Username : root
# Password : secret
# Database : node-complete
```

## Database.js example

```javascript
const mysql = require("mysql2");

const pool = mysql.createPool({
  host: "localhost",
  user: "root",
  password: "secret",
  database: "node-complete",
});

module.exports = pool.promise();
```
