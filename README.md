yarn add strapi-plugin-ckeditor5
yarn build --clean

grant all privileges on database strapi to strapi;
alter user strapi with encrypted password 'strapi123';

psql -U postgres
\du // lista permissoes
\l lista os database

yarn develop se der erro no sharp remover node_modules
psql -h localhost -U postgres -d strapi -W < strapi.sql

pg_dump -c --if-exists --exclude -table=strapi_admistrator -h 127.0.0.1 -U strapi -d strapi -W > strapi.sql

heroku config:set DATABASE_USERNAME=fqmuewmhzucwoe

heroku config:set DATABASE_PASSWORD=02ae302647d962b58631bf6436fe32dfed1733348b6862f6ec19f59663ce4f20

heroku config:set DATABASE_HOST=ec2-3-218-71-191.compute-1.amazonaws.com

heroku config:set DATABASE_PORT=5432

heroku config:set DATABASE_NAME=fqmuewmhzucwoe

heroku config:set CLOUDINARY_NAME=dzgzmimb1
heroku config:set CLOUDINARY_KEY=389859984251389
heroku config:set CLOUDINARY_SECRET=sYEQTmZszb3lLQKYTxqX7cCAsDY


postgres://fqmuewmhzucwoe:02ae302647d962b58631bf6436fe32dfed1733348b6862f6ec19f59663ce4f20@ec2-3-218-71-191.compute-1.amazonaws.com:5432/damsultrc0eikp

git push heroku HEAD:main


heroku config:set NODE_ENV=production
heroku config:set MY_HEROKU_URL=https://reactavancado-api-perosa.herokuapp.com/
heroku config:set ADMIN_JWT_SECRET=ZbipfvmcVQttdAwYlpSSLbw7MyckbHQPajxWadibFvsL8VlBox+8yb3k+ZOBnWuma/W1IwB62V1Xipz6dZBMHA==

pg_dump -Fc --no-acl --no-owner -h localhost -U strapi strapi > strapi.dump

heroku pg:backups:restore 'https://reactavancado-assets.s3.us-east-2.amazonaws.com/mydb.dump' DATABASE_URL
heroku pg:psql < strapi.dump

