# react-beforeunload

React component which listens to `beforeunload` on the window when mounted.

## Usage

### `Beforeunload` Component

Import as default or named export:

```
import Beforeunload from 'react-beforeunload';
// or
import { Beforeunload } from 'react-beforeunload';
```

Display a dialog box:

```jsx
<Beforeunload onBeforeunload={event => event.preventDefault()} />
```

Display a dialog box with custom message:

```jsx
<Beforeunload onBeforeunload={() => "You'll lose your data!"} />
```

> Some browsers display the returned string in the dialog box, others display a fixed message.

[Source](https://developer.mozilla.org/en-US/docs/Web/Events/beforeunload)

Or use as a wrapper:

```jsx
<Beforeunload onBeforeunload={…}>
  <MyApp />
</Beforeunload>
```

### `useBeforeunload` Hook

Import as named export:

```
import { useBeforeunload } from 'react-beforeunload';
```

And use as you would use the component:

```jsx
useBeforeunload(event => event.preventDefault());
```

```jsx
useBeforeunload(() => "You'll lose your data!");
```

## Requirements

Requires a minimum of React version 16.8.0. If you're on an older version of React, then checkout [v1](https://github.com/jacobbuck/react-beforeunload/tree/v1).
