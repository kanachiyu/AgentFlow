# agent-flow

A simple library to run sequences of tasks using LLMs.

### Install

```bash
npm install agent-flow
```

### Usage

```javascript
const { AgentFlow } = require('agent-flow');

const flow = new AgentFlow();

flow.add(async () => 'Step 1 output');
flow.add(async (prev) => `Processed: ${prev}`);

const result = await flow.run();
console.log(result);
```

### License

MIT
