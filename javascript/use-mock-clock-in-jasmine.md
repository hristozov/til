# Use a mock clock in Jasmine (2016-02-15)
Jasmine (1.3, in this case) allows you to [mock the clock](https://jasmine.github.io/1.3/introduction.html#section-Mocking_the_JavaScript_Clock):

```javascript
beforeEach(() => {
    jasmine.Clock.useMock();
});

it('should do awesome stuff', () => {
    var awesome = false;

    setTimeout(() => {
                   awesome = true;
               },
               60000);
    expect(awesome).toEqual(false);

    jasmine.Clock.tick(60000);
    expect(awesome).toEqual(true);
});
```
Of course, this test won't run for 60 seconds. For this reason, using mock clock should be preferred over setting timeouts with expectations.
