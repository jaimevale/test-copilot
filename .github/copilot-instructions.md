Este es un proyecto gradle java que utiliza un plugin llamado "Clean Architecture" y que utiliza estas tasks para crear sus componentes.
Para crear el proyecto se utiliza gradle cleanArchitecture, asi

    gradle cleanArchitecture --package=com.vcsoft.copilot --type=reactive --name=TestCopilot --lombok=true

Para crear un modelo se utiliza la siguiente linea cambiando modelName por el nombre del modelo

    gradle generateModel --name=modelName

Para crear un caso de uso se utiliza la siguiente linea cambiando useCaseName por el nombre del caso de uso
    gradle generateUseCase --name=useCaseName 

The generateDrivenAdapter  task will generate a module using a repository defined by drivenAdapterType parameter. the values are dynamodb,jpa,mongodb,r2dbc,redis,s3 the default value is r2dbc

   gradle generateDrivenAdapter --type=drivenAdapterType

The generateEntryPoint task will generate the rest interface using the entryPointType value as webflux or graphql. Use the default value webflux.

    gradle generateEntryPoint --type=entryPointType

