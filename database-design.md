## 一. 文章分类、文章、轮播图

### 文章一级分类信息表（cf_article_first_classify）

| **字段名**       | **注释** | **属性** | **长度** | **是否为主键** | **是否为空** | **备注**                                              |
| ---------------- | -------- | -------- | -------- | -------------- | ------------ | ----------------------------------------------------- |
| id               | 主键     | varchar  | 36       | Y              | N            |                                                       |
| first_class_name | 分类名称 | varchar  | 36       | N              | Y            |                                                       |
| class­_number    | 分类编号 | int      | 2        | N              | N            |  |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


### 文章二级分类信息表（cf_article_second_classify）

| **字段名**        | **注释**   | **属性** | **长度** | **是否为主键** | **是否为空** | **备注** |
| ----------------- | ---------- | -------- | -------- | -------------- | ------------ | -------- |
| id               | 编号       | varchar  | 36       | Y              | N            |          |
| second_class_name | 分类名称   | varchar  | 36       | N              | Y            |          |
| class_number      | 序号       | Int      | 11       | N              | Y            |          |
| first_classify_id | 一级分类ID | varchar  | 36       | N              | N            |          |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


### 文章表（cf_article）

| 字段名       | **注释** | **属性** | **长度** | **是否为主键** | **是否为空** | **备注** |
| ------------ | -------- | -------- | -------- | -------------- | ------------ | -------- |
| id           | 主键id   | varchar  | 36       | Y              | N            |          |
| cover_path | 封面路径 | varchar  | 255     | N              | Y            |          |
| article_title         | 文章标题 | varchar  | 255      | N              | Y            |          |
| article_content        | 内容 | varchar  | 9999      | N              | Y            |          |
| first_classify_id | 一级分类ID | varchar  | 36       | N              | N            |          |
| second_classify_id | 二级分类ID | varchar  | 36       | N              | N            |          |
| article_source         | 来源     | varchar      | 255        | N              | Y            |  |
| release_date         | 发布日期     | datetime      |        | N              | Y            |  |
| is_shown         | 是否显示     | int      | 2        | N              | Y            | 0.        隐藏   1.        显示 |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


### 轮播图表(cf_carousel)

| **字段名**       | **注释**     | **属性** | **长度** | **是否为主键** | **是否为空** | **备注**                        |
| ---------------- | ------------ | -------- | -------- | -------------- | ------------ | ------------------------------- |
| id               | 编号         | varchar  | 36       | Y              | N            |                                 |
| path             | 轮播图路径   | varchar  | 255      | N              | Y            |                                 |
| caroursel_number | 序号         | Int      | 11       | N              | Y            |                                 |
| is_shown         | 是否显示     | int      | 2        | N              | Y            | 0.        隐藏   1.        显示 |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


## 二. 捐赠信息、求助信息、意见反馈

###  捐赠信息（cf_giving_information）

| 字段名       | **注释** | **属性** | **长度** | **是否为主键** | **是否为空** | **备注** |
| ------------ | -------- | -------- | -------- | -------------- | ------------ | -------- |
| id           | 主键id   | varchar  | 36       | Y              | N            |          |
| giving_information_title | 标题 | varchar  | 1000     | N              | Y            |          |
| giver_name         | 捐赠人 | varchar  | 255      | N              | Y            |          |
| giving_property_information        | 捐赠财物信息 | varchar  | 500      | N              | Y            |          |
| giving_information_content    | 信息详情 | varchar  | 255      | N              | Y            |          |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


### 求助信息（cf_help_information）

| 字段名       | **注释** | **属性** | **长度** | **是否为主键** | **是否为空** | **备注** |
| ------------ | -------- | -------- | -------- | -------------- | ------------ | -------- |
| id           | 主键id   | varchar  | 36       | Y              | N            |          |
| help_information_title | 标题 | varchar  | 1000     | N              | Y            |          |
| seeker_name         | 求助人 | varchar  | 255      | N              | Y            |          |
| seek_property_information         | 求助财物信息 | varchar  | 500      | N              | Y            |          |
| help_information_content    | 信息详情 | varchar  | 255      | N              | Y            |          |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |


### 意见反馈（cf_feedback）

| 字段名       | **注释** | **属性** | **长度** | **是否为主键** | **是否为空** | **备注** |
| ------------ | -------- | -------- | -------- | -------------- | ------------ | -------- |
| id           | 主键id   | varchar  | 36       | Y              | N            |          |
| feedback_content | 反馈内容 | varchar  | 1000     | N              | Y            |          |
| ip_address         | ip地址 | varchar  | 50      | N              | Y            |          |
| create_date      | 创建日期 | datetime |          | N              | Y            |                                                       |
| update_date      | 更新日期 | datetime |          | N              | Y            |                                                       |
