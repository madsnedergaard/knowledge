---
description: 'Best practices, handy tools and snippets, etc.'
---

# Testing JavaScript

### Best Practices

{% hint style="info" %}
_The following best practices are very inspired by_ [_Yoni Goldberg's ideas_](https://github.com/goldbergyoni/javascript-testing-best-practices)
{% endhint %}

#### 1. Design for lean testing

* Keep tests as simple as possible!
* Avoid "smart" abstractions - DRY is not the goal here

It's better to have 90% coverage in simple, easy-to-read tests than to have 100% coverage with tests that takes a lot of mental effort to understand.


---

#### 2. AAA pattern

- Acquire, Act, Assert


### Snippets



### How to ...

#### Mock express routes

```javascript
// Util for mocking req
const mockRequest = (options) => ({
  ...options,
});

// Util for mocking res
const mockResponse = () => {
  const res = {};
  res.json = jest.fn().mockReturnValue(res);
  res.send = jest.fn().mockReturnValue(res);
  res.status = jest.fn().mockReturnValue(res);
  return res;
};

it('tests myEndpoint', async () => {
  const req = mockRequest({ body: { name: 'test' } });
  const res = mockResponse();

  await myEndpoint(req, res);

  expect(res.status).toHaveBeenCalledWith(200);
  expect(res.json).toHaveBeenCalledWith({
    message: 'Success',
  });
});
```





### Links

{% embed url="https://github.com/goldbergyoni/javascript-testing-best-practices" %}



