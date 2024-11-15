graph TD
    subgraph Cliente
        PC[Cliente PC]
        Movil[Cliente Móvil]
    end

    subgraph API Gateway
        Gateway[API Gateway]
    end

    subgraph Backend
        ClientesSvc[Microservicio Clientes]
        PedidosSvc[Microservicio Pedidos]
        RepartoSvc[Microservicio Reparto y Rutas]
        EstadisticasSvc[Microservicio Estadísticas]
        IncidenciasSvc[Microservicio Incidencias]
        PagosSvc[Microservicio Pagos]
    end

    %% Conexiones de Cliente a Gateway
    PC -->|HTTP/REST| Gateway
    Movil -->|HTTP/REST| Gateway

    %% Conexiones de Gateway a Backend
    Gateway --> ClientesSvc
    Gateway --> PedidosSvc
    Gateway --> RepartoSvc
    Gateway --> EstadisticasSvc
    Gateway --> IncidenciasSvc
    Gateway --> PagosSvc

    %% Conexiones entre microservicios
    PedidosSvc --> RepartoSvc
    PedidosSvc --> IncidenciasSvc
    RepartoSvc --> IncidenciasSvc
    RepartoSvc --> EstadisticasSvc
    IncidenciasSvc --> EstadisticasSvc
    ClientesSvc --> EstadisticasSvc

    %% Pasarela de pagos
    PagosSvc -->|API de MercadoPago| ML([Pasarela de pago MercadoPago])
    PedidosSvc --> PagosSvc
