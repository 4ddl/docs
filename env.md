# 部署过程中，需要后台配置的环境变量

## Postgres
| 键 | 默认值 | 必须 | 备注 |
| --- | --- | --- | --- |
| POSTGRES_DB | ` ` | 是 | 数据库名称 |
| POSTGRES_USER | `postgres` | 否 | 数据库用户 |
| POSTGRES_PASSWORD | ` ` | 是 | 数据库密码 |

## RabbitMQ

| 键 | 默认值 | 必须 | 备注 |
| --- | --- | --- | --- |
| RABBITMQ_DEFAULT_USER | `guest` | 否 | 默认用户 |
| RABBITMQ_DEFAULT_PASS | `guest` | 否 | 默认密码 |

## Backend

| 键 | 默认值 | 必须 | 备注 |
| --- | --- | --- | --- |
| DDL_ENV | `production` | 否 | 工作环境 |
| DDL_DEBUG | `False` | 否 | 是否debug |
| REDIS_HOST | `127.0.0.1` | 否 | Redis的主机 |
| REDIS_PORT | `6379` | 否 | Redis的端口 |
| POSTGRES_HOST | `127.0.0.1` | 否 | Postgres的主机 |
| POSTGRES_PORT | `5432` | 否 | Postgres的端口 |
| POSTGRES_DB | `ddl` | 否 | Postgres的数据库名称 |
| POSTGRES_USER | `postgres` | 否 | Postgres的用户 |
| POSTGRES_PASS | `password` | 否 | Postgres的密码 |
| RABBITMQ_HOST | `127.0.0.1` | 否 | RabbitMQ的主机 |
| RABBITMQ_PORT | `5672` | 否 | RabbitMQ的端口 |
| RABBITMQ_USER | `guest` | 否 | RabbitMQ的用户 |
| RABBITMQ_PASS | `guest` | 否 | RabbitMQ的密码 |
| JUDGE_TOKEN | `JUDGE_TOKEN` | 否 | 判题机请求数据的Token |
| SECRET_KEY | `THIS_IS_A_SECRET_KEY` | 否 | Django数据库的salt |
| EMAIL_ENABLE | `False` | 否 | 允许真实的邮箱，否则的话只会在控制台打印，用户收不到真正的邮箱验证码 |
| EMAIL_HOST | ` ` | 是 | 邮箱的smtp服务器地址 |
| EMAIL_PORT | `465` | 否 | 邮箱的smtp服务器的端口，只有465端口支持SSL |
| EMAIL_HOST_USER | ` ` | 是 | 邮箱用户 |
| EMAIL_HOST_PASSWORD | ` ` | 是 | 邮箱用户的密码 |

## Judge

| 键 | 默认值 | 必须 | 备注 |
| --- | --- | --- | --- |
| DDLCW_DEBUG | `False` | 否 | 是否开启debug |
| DDLCW_ENABLE_SYNC | `False` | 否 | 是否允许同步测试数据 |
| JUDGE_TOKEN | `JUDGE_TOKEN` | 否 | 判题机请求数据的Token |
| BROKER_URL | `amqp://guest:guest@127.0.0.1:5672/` | 否 | 判题机的RabbitMQ地址 |
| BACKEND_URL | `http://127.0.0.1` | 否 | 请求后台题目的host |
