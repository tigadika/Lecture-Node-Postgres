table `GirlGroups`

| column_name | type    | constraints |
| ----------- | ------- | ----------- |
| id          | serial  | primary key |
| name        | varchar | not null    |
| member      | integer | not null    |
| company     | varchar | not null    |
| debutSong   | text    | -           |