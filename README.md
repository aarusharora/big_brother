# big_brother
Repo for learning and research findings


- Python
  - Pacakge management
    - pipenv: pipenv install <package_name>[standard/all]
  - Testing
    - Pytest: 
      - Links: 
        - [Pytest](https://docs.pytest.org/en/7.2.x/getting-started.html)
        - [Conventions for Test Discovery](https://docs.pytest.org/en/7.2.x/explanation/goodpractices.html#test-discovery)
      - File name starts with `test_*.py` or `*_test.py` in current dir and subdirs.
      - function name starts with `test_*`
      - Prefix custom test class name with `Test*`
      - assert sum(3,2) == 5
      - `-q` for quiet mode
      - able to group multiple tests in class.
      - pytest -q test_file.py
      - pytest --fixtures -v # to see fixtures and built-in functions
    - FastAPI: 
      - Links:
        - [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/)
      - import TestClient from the `fastapi` package - `from fastapi.testclient import TestClient`.
      - standard pytest naming conventions for functions.
      - Testing functions are `def` not `async def`.
      - `client = TestClient(FastAPI())`, `response = client.get('/')`, `assert response.status_code == 200`
      - calls to the `client.get()` are normal calls, not with `await`. client is basically a requests object now.
