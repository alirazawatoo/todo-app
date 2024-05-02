# Task Management API

A Rails JSON API for user registration, sessions, and authenticated task CRUD. Tasks include title, description, due date, and completion state.

```text
register / sign in -> authenticated user -> create, list, update, complete, delete tasks
```

Controllers live under `app/controllers/api/v1`, account endpoints use registration/session controllers, and serializers define task/user responses. The matching client is [`to_do_app_frontend`](https://github.com/alirazawatoo/to_do_app_frontend).

```bash
bundle install
rails db:create db:migrate db:seed
rails server
```

Configure PostgreSQL and local environment values first. Model and controller specs are included but were not run. Every task lookup should remain scoped to the signed-in user; production also needs secure secrets, restricted CORS, expiry decisions, rate limiting, and consistent JSON errors.
