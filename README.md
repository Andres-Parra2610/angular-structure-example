# Project Structure Overview

This Angular project utilizes a blend of both standalone components and NgModules to achieve modularity and reusability across different parts of the application. The structure is designed to accommodate specific features for different clients by lazily loading client-specific modules, enhancing the application's scalability and maintainability.

## src/app

### Modules

Located under the `src/app/modules`, this directory contains all the NgModules of the application. Each module corresponds to a distinct functional area of the application, such as login handling, map functionalities, etc. Add modules that are relevant into application.

#### Example Modules:

- **Login**: Handles user authentication.
- **Maps**: Manages all map-related functionalities.
- **Monitoring**: Weed monitoring
- **Planification**: Activities planning
- **Warehouses**: Manages inventory and warehouse-related operations.
- **Ohers**: Other modules

### Shared

The `src/app/shared` directory is pivotal for housing reusable components and helpers that are not tied to specific modules. This folder also contains standalone components, which can be utilized throughout the application without the dependency on an overarching module

#### Example Components:
- **Charts**: Reusable chart components for visual data representation.
- **Inputs**: Custom input components for forms.

#### Helpers:
General utility functions and classes that assist in common tasks across the application.

### Users

Each client has a dedicated subdirectory within the `src/app/users`, which contains modules specific to them. These modules are loaded lazily, ensuring that the application remains efficient by only loading the necessary resources when required.

#### Example Clients:
- **Danac**
- **Polar**

Each client directory can include a custom set of modules that are relevant to the client's needs, ensuring a tailored user experience.
