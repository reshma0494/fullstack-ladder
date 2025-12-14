Context:
This project consists of small number of views like creating issues, listing/updating them in board layout. Although its UI is simple, multiple components (forms, columns, cards, filters) need to read and update data in structured way.

Decision:
I chose React's built-in useReducer for state management.

Rationale:
useReducer provides action based updates and predictable state transitions in this application. useState will be more localized and will make it tough to test/update state in multiple components. Introducing libraries like Redux toolkit or Zustand would be an overkill and increase overhead for a small single page application.

Consequences:
If app grows in size, adapting a state management library would be a better approach since handling state across multiple pages and across widely spread features would be easier.
