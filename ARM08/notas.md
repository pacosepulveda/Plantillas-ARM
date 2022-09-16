You set the scope through the expressionEvaluationOptions property. By default, the expressionEvaluationOptions property is set to outer, which means it uses the parent template scope. Set the value to inner to cause expressions to be evaluated within the scope of the nested template.
Por ejemplo, si definimos un parámetro en la plantilla padre y necesitamos usar ese parámetro en la plantilla anidada, el scope en expressionEvalutionOptions de la plantilla anidada debe ser "outer". De lo contrario, no encontrará el parámetro.

La plantilla de la sección "Nested template example" debe desplegarse a nivel de suscripción:
New-AzDeployment -Name "despliegue-suscripcion" -TemplateFile .\azuredeploy.json -Location eastus2
