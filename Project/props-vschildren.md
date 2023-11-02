# React: props vs Children

```jsx
import React from 'react';

function DisplayInfo(props) {
  return (
    <div className="info-card">
      <h2>{props.title}</h2>
      <p>{props.description}</p>
      {props.children}
    </div>
  );
}

function App() {
  return (
    <div>
      <DisplayInfo title="Person 1" description="Info about Person 1">
        <p>Additional info for Person 1.</p>
      </DisplayInfo>

      <DisplayInfo title="Person 2" description="Info about Person 2">
        <p>Additional info for Person 2.</p>
      </DisplayInfo>
    </div>
  );
}

export default App;
```

In this simplified version, we've used `props` directly in the `DisplayInfo` component without destructuring for brevity. The `children` and regular props are still used as in the previous example to pass content and data to the component.