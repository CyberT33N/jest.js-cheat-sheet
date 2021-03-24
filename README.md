# Jest.js Cheat Sheet
Jest.js Cheat Sheet with the most needed stuff..



<br />
<br />


 _____________________________________________________
 _____________________________________________________


<br />
<br />

# Expect (https://jestjs.io/docs/en/expect)
```bash
npm i expect --save-dev
```
```javascript
const expect = require('expect');
```

<br>
<br>

## .toBe
```javascript
// Use .toBe to compare primitive values or to check referential identity of object instances. It calls Object.is to compare values, which is even better for testing than === strict equality operator.
const add = (a, b) => a + b;
expect( add(2, 3) ).toBe(5);
expect( typeof add(2, 3) ).toBe('number');
```

<br>
<br>

## .toEqual (https://jestjs.io/docs/en/expect#toequalvalue)
```javascript
// Use .toEqual to compare recursively all properties of object instances (also known as "deep" equality). It calls Object.is to compare primitive values, which is even better for testing than === strict equality operator.
expect( {a: undefined, b: 2} ).toEqual( {b: 2} );
```

## .toStrictEqual (https://jestjs.io/docs/en/expect#tostrictequalvalue)
```javascript
// test that objects have the same types as well as structure. Check above .toEqual for compare difference
expect( {"test": 1} ).toStrictEqual( {"test": 1} );
```


<br>
<br>


## .objectContaining (https://jestjs.io/docs/en/expect#expectobjectcontainingobject)
```javascript
/*expect.objectContaining(object) matches any received object that recursively matches the expected properties. That is, the expected object is a subset of the received object. Therefore, it matches a received object which contains properties that are present in the expected object.

Instead of literal property values in the expected object, you can use matchers, expect.anything(), and so on.*/
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.any(Number),
    geo: expect.any(Array),
    isFetching: expect.any(Boolean)
}));
```


<br>
<br>

## .any (https://jestjs.io/docs/en/expect#expectanyconstructor)
```javascript
// expect.any(constructor) matches anything that was created with the given constructor. You can use it inside toEqual or toBeCalledWith instead of a literal value.
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.any(Number)
}));
```

## .anything (https://jestjs.io/docs/en/expect#expectanything)
```javascript
// expect.anything() matches anything but null or undefined. You can use it inside toEqual or toBeCalledWith instead of a literal value. For example, if you want to check that a mock function is called with a non-null argument:
expect( location() ).toEqual(expect.objectContaining({
    locationId: expect.anything()
}));
```


<br><br>



## .toBeTruthy (https://jestjs.io/docs/en/expect#tobetruthy)
```javascript
// Use .toBeTruthy when you don't care what a value is and you want to ensure a value is true in a boolean context. 
expect( location() ).toBeTruthy();
```

<br><br>



## .toMatch (https://jestjs.io/docs/en/expect#tomatchregexp--string)
```javascript
// Use .toMatch to check that a string matches a regular expression.
expect( getDate() ).toMatch(/\d\d\/\d\d\/\d\d\d\d/gmi);
```

<br><br>

## .include (https://www.chaijs.com/api/bdd/#method_include)
```javascript
expect('foobar').to.include('foo');

expect([1, 2, 3]).to.include(2);
```









<br><br>




## Operators
```javascript
// You can use operators to check for multiple conditions
expect(msg).toEqual( expect.objectContaining({date: expect.anything()}) &&
expect.objectContaining({msg: expect.anything()}) &&
expect.objectContaining({room: expect.anything()}) &&
expect.objectContaining({usertoken: expect.anything()}) );
```
