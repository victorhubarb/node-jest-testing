# Node Jest Testing

A small REST API for a bookstore (books, authors, publishers) built with Express and SQLite, used to practice automated testing with Jest and Supertest. The tests cover the publishers (`editoras`) resource, both the model and the HTTP routes.

## What's tested

- **Model, unit level** (`src/test/models/editora.test.js`): that an `Editora` is built with the right fields, and a mocked `salvar()` using `jest.fn().mockReturnValue(...)`, so no database is touched. Two further tests that hit the real database are marked `it.skip`.
- **Routes, integration level** (`src/test/routes/editorasRoutes.test.js`): Supertest sends real requests to the Express app and checks status codes and bodies.
  - `GET /editoras` returns JSON with a 200
  - `POST /editoras` returns 201 for a valid body and 400 for an empty one
  - `GET /editoras/:id` returns the record that was just created
  - `PUT /editoras/:id` is parameterized with `test.each` over name, city and email, and uses `jest.spyOn`
  - `DELETE /editoras/:id` cleans up the record the POST test made

The route tests run against the SQLite file in `src/db/livraria.sqlite`. Because they create and then delete their own record, the database ends up as it started.

## The API

```
GET|POST         /livros   /autores   /editoras
GET|PUT|DELETE   /livros/:id   /autores/:id   /editoras/:id
GET              /autores/:id/livros   /editoras/:id/livros
```

It follows a model, controller and routes layout, with Knex as the query builder. `populate.sql` holds the schema and seed data. The messages in the code are in Portuguese.

## Run it

Requires Node.js 18 (the pinned `sqlite3` version is old, so a newer Node may have to compile it).

```bash
git clone https://github.com/victorhubarb/node-jest-testing.git
cd node-jest-testing
npm install

npm test        # Jest with ES modules, verbose output
npm run dev     # API on http://localhost:3000 with nodemon
```

## Known gaps

- Only `editoras` has tests. `livros` and `autores` have none.
- The routes tests expect the first seeded publisher to have the email `e@e.com`, so they depend on the committed database.
- `GET /editoras/:id/livros` reads `resultado[0]` from an object, so the `editora` field comes back empty. It needs a test and a fix.
- `PUT` answers 204 and also tries to send a JSON body, which clients will not receive.
- No coverage report is configured.

---

Victor Hugo Barbosa · [GitHub](https://github.com/victorhubarb) · [LinkedIn](https://www.linkedin.com/in/victorhbarbosa/)
