# Jasmine JSON Fixtures

```javascript
describe('my tests', function() {
	// base path to test fixtures
	jasmine.getFixtures().fixturesPath = 'base/fixtures/';
	
	describe('something I need to test', function() {
		// will get "base/fixtures/some/mockup/file.json" before run the tests
		beforeEach(loadJSONFixture('some/mockup/file.json'));

		it('should run the test', function() {
			var fixture = getJSONFixture('some/mockup/file.json');
			// ...
		});
	});
});
```

## NOTES

	Requires Jasmine 2.0+ to work!

The `beforeEach` handler will use the async syntax of Jasmine to hold the test suite until the JSON file is loaded