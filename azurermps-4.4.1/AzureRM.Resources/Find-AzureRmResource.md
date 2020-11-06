---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429130"
---
# Find-AzureRmResource

## Sinopse
Pesquisa recursos com base em parâmetros especificados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Lista os recursos com base no escopo especificado. Assume
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Lista os recursos com base no escopo especificado no nível do locatário.
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Obter recursos usando uma consulta de várias assinaturas.
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Lista os recursos por um objeto de marca especificado como um HashSet.
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Lista os recursos por uma marca especificada como um nome individual e parâmetros de valor.
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Find-AzureRmResource** pesquisa recursos com base em parâmetros especificados.

## EXEMPLOS

### Exemplo 1: procurar recursos por tipo e nome do grupo de recursos
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

Esse comando pesquisa recursos do tipo Microsoft. Web/sites em grupos de recursos que têm nomes que correspondem à cadeia de caracteres do grupo de fontes.

### Exemplo 2: pesquisar recursos por tipo e nome do recurso
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

Esse comando pesquisa recursos do tipo Microsoft. Web/sites que têm um nome de recurso que corresponda ao teste de cadeia de caracteres.

## OS

### -ApiVersion
Especifica a versão da API do provedor de recursos a ser usada.
Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.

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

### -Expandproperties
Indica que esse cmdlet expande as propriedades do recurso.

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

### -ExtensionResourceType
Especifica o tipo de recurso de extensão para os recursos para os quais esse cmdlet pesquisa.
Por exemplo:

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
Especifica um filtro de estilo Open Data Protocol (OData).
Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.

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

### -Pre
Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.

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

### -ResourceGroupNameContains
Especifica um nome parcial de um grupo de recursos.
Este cmdlet corresponde a grupos de recursos dos quais esse valor é uma subcadeia de caracteres.
O cmdlet pesquisa recursos nesses grupos de recursos.

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupNameEquals
O nome do grupo de recursos para uma correspondência completa.

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceNameContains
Especifica um nome parcial de um recurso.
O cmdlet pesquisa recursos que contêm esse valor como uma subcadeia de caracteres.

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceNameEquals
O nome do recurso para uma correspondência completa. por exemplo, se o nome do recurso for testResource, você poderá especificar testResource.

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Especifica o tipo de um recurso.
Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:

`Microsoft.Sql/Servers/Databases`

Este cmdlet procura recursos do tipo especificado.

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
O filtro de marca para a consulta OData. O formato esperado é @ {tagName = $null} ou @ {tagName = ' tagValue '}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TagName
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TagValue
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantLevel
Indica que esse cmdlet opera no nível do locatário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Início
Especifica o número de recursos a serem recuperados.

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Management. Automation. PSObject

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Mover-AzureRmResource](./Move-AzureRmResource.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[Remove-AzureRmResource](./Remove-AzureRmResource.md)

[Set-AzureRmResource](./Set-AzureRmResource.md)
