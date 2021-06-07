yarn add strapi-plugin-ckeditor5
yarn build --clean

grant all privileges on database strapi to strapi;
alter user strapi with encrypted password 'strapi123';

psql -U postgres
\du // lista permissoes
\l lista os database

yarn develop se der erro no sharp remover node_modules
psql -h localhost -U postgres -d strapi -W < strapi.sql

pg_dump -c --if-exists --exclude
-table=strapi_admistrator -h 127.0.0.1 -U strapi -d strapi -W > strapi.sql
