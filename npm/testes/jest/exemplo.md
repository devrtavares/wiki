# nodejs 

<sub>[:arrow_upper_left: jest](readme.md)<sub>

## *jest.config.js - exemplo*


```json
module.exports = {
	roots: [
		"<rootDir>/src"
	],
	collectCoverageFrom: ['<rootDir>/src/**/*.ts'],
	coverageDirectory: "coverage",
	testEnvironment: 'node',
	transform: {
		'.+\\.ts$': 'ts-jest'
	},
	collectCoverage: true,
	clearMocks: true,
	coverageProvider: "v8",
}
```