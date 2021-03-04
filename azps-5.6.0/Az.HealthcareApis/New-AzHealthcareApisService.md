---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: e99c060cc7446cbecc46040ec4a498cf9f545e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893299"
---
# New-AzHealthcareApisService

## SYNOPSIS
Cria os metadados de uma instância de serviço.

## SINTAXE

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
Cria ou atualiza os metadados de uma instância de serviço.

## EXEMPLOS

### Exemplo 1 : cria um novo serviço do Azure healthcareapis fhir chamado MyService no grupo de recursos MyResourceGroup em um local westus2 com a produtividade da oferta do cosmosdb = 400
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### Exemplo 2 : cria um novo serviço do Azure healthcareapis fhir chamado MyService no grupo de recursos MyResourceGroup em um local westus2 com a produtividade da oferta do cosmosdb = 400 e uri de chave de chave de cofre "https:// \<my-keyvault> .vault.azure.net/keys/ \<my-key> "
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## PARÂMETROS

### -AccessPolicyObjectId
Lista de IDs de objeto da Política de Acesso.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCorsCredential
HealthcareApis Fhir Service AllowCorsCredentials.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Execute o cmdlet como um trabalho em segundo plano.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Audience
HealthcareApis Fhir Service Audience.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Authority
Autoridade de Serviço HealthcareApis Fhir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorsHeader
HealthcareApis Fhir Service List of Cors Header.
Especifique cabeçalhos HTTP que podem ser usados durante a solicitação.
Use " * " para qualquer header.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorsMaxAge
HealthcareApis Fhir Service Cors Max Age.
Especifique por quanto tempo um resultado de uma solicitação pode ser armazenado em cache em segundos.
Exemplo: 600 significa 10 minutos.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorsMethod
HealthcareApis Fhir Service List of Cors Method.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorsOrigin
HealthcareApis Fhir Service List of Cors Origin.
Especifique URLs de sites de origem que possam acessar essa API ou use " * " para permitir o acesso de qualquer site.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CosmosKeyVaultKeyUri
HealthcareApis Fhir Service CosmosKeyVaultKeyUri.
O URI da chave gerenciada pelo cliente para o banco de dados de suporte.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CosmosOfferThroughput
HealthcareApis Fhir Service CosmosOfferThroughput.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSmartProxy
Serviço HealthcareApis Fhir EnableSmartProxy.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExportStorageAccountName
HealthcareApis Fhir Service Export Storage Account Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FhirVersion
Versão Fhir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Tipo de Serviço HealthcareApis.
O valor padrão é Fhir

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Local do serviço HealthcareApis.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedIdentity
Usar Identidade Gerenciada?

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome do serviço HealthcareApis.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
O tipo de acesso à rede para o serviço Fhir. Normalmente `Enabled` ou `Disabled` .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do Grupo de Recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Marcas de conta de serviço HealthcareApis Fhir.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService

## NOTES

## LINKS RELACIONADOS
