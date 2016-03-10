# (work in progress), a router for React

What makes this router different is the ability to encode routes and nest them within other routes, to infinite depth. Why does that make sense? Because a rendering tree is just that – a tree structure. What happens when you sometimes want to render Component `A` in layout `B`, and other times in layout `C`? You end up with MxN routes, and poor re-usability (needing to re-map Component `A`s routes and sub-routes in the new location).  

This is a router with first-class support for components and layouts. Any component or layout can be assigned to a route. When a component is assigned to a route, the route can contain parameters that are mapped to component props.  When a layout is assigned to a route, the route can contain sub-routes specifying what should be rendered in the available layout regions. This makes it extremely scalable to do things like render a specific component within different application routes (and layouts), and 
