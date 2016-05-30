# loadimpact-api-doc


```
{
  "modules": [{ModuleType}],
  "LuaModules": [{LuaModuleType}]
}
```



ModuleType:
* id
* title
* description
* apis: ARRAY[ApiType]
* classes: ARRAY
  - id
  - name
  - longName
  - description
  - apis: ARRAY[ApiType]
  - attributes: ARRAY[ParameterType]
  - examples: ARRAY[ExampleType]
* enums: ARRAY [{id, longName, description}]
* examples: ARRAY[ExampleType]
* notes: ARRAY [string]


LuaModuleType:
* id
* name
* description
* modules: ARRAY
  - id
  - name
  - moduleName
  - apis: ARRAY [{name, link}]


ApiType:
- id
- name
- longName
- description
- parameters: ARRAY[ParameterType]
- returns: string
- options: ARRAY[{name, parameters = ARRAY[ParameterType]}]
- examples: ARRAY[ExampleType]

ExampleType:
- id (optional)
- title (optional)
- content: ARRAY[string]

ParameterType:
- name
- type
- description
