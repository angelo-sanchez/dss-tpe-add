```mermaid
sequenceDiagram
    participant Client
    participant RouteHandler
    participant RouteCache
    participant AbstractRouteCalculator
    participant RouteRequest
    participant Route


    Client->>RouteHandler: Instantiate RouteHandler
    Note over RouteHandler: Contains cache (RouteCache)


    Client->>RouteRequest: Create RouteRequest
    Client->>AbstractRouteCalculator: Instantiate Calculator (e.g., ShortestTimeAlgorithm)
    Client->>RouteHandler: handleRoute(request, calculator)


    RouteHandler->>RouteCache: getRoute(request)
    RouteCache-->>RouteHandler: Route (if cached) or null


    alt Route cached
        RouteHandler-->>Client: Return cached Route
    else Route not cached
        RouteHandler->>AbstractRouteCalculator: calculateRoute(request)
        AbstractRouteCalculator->>AbstractRouteCalculator: preProcess(request)
        AbstractRouteCalculator->>AbstractRouteCalculator: executeAlgorithm(request)
        AbstractRouteCalculator->>AbstractRouteCalculator: postProcess(route)
        AbstractRouteCalculator-->>RouteHandler: Route


        RouteHandler->>RouteCache: Cache the new Route
        RouteHandler-->>Client: Return new Route
    end
```
