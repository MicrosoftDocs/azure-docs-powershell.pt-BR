---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259319"
---
# New-AzCustomProvider

## Sinopse
Cria ou atualiza o provedor de recursos personalizado.

## SYNTAX

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Cria ou atualiza o provedor de recursos personalizado.

## EXEMPLOS

### Exemplo 1: criar um provedor personalizado
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Criar um provedor de recursos personalizado

### Exemplo 2: criar um provedor personalizado com associações
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Crie um provedor personalizado, com uma rota para associações de provedor personalizado.

## OS

### -Ação
Uma lista de ações implementadas pelo provedor de recursos personalizados.
Para construir, consulte a seção observações para propriedades de ação e criar uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Executar o comando como um trabalho

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Local do recurso

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do provedor de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Executar o comando de forma assíncrona

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

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Uma lista de tipos de recurso implementados pelo provedor de recursos personalizados.
Para construir, consulte a seção de observações para as propriedades de RESOURCETYPE e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura do Azure.
Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Marcas de recurso

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Validação
Uma lista de validações a serem executadas nas solicitações do provedor de recursos personalizado.
Para construir, consulte a seção de notas para propriedades de validação e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


AÇÃO <ICustomRpActionRouteDefinition [] >: uma lista de ações implementadas pelo provedor de recursos personalizados.
  - `Endpoint <String>`: O URI de ponto de extremidade de definição de rota ao qual o provedor de recursos personalizado fará a solicitação de proxy. Isso pode ser na forma de um URI simples (por exemplo, ' https://testendpoint/ ') ou pode especificar a rota por meio de um caminho (por exemplo, ' https://testendpoint/{requestPath} ')
  - `Name <String>`: O nome da definição de roteiro. Isso se torna o nome da extensão do braço (por exemplo, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ActionRouting?>]`: Os tipos de roteamento com suporte para solicitações de ação.

RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: uma lista de tipos de recursos que o provedor de recursos personalizado implementa.
  - `Endpoint <String>`: O URI de ponto de extremidade de definição de rota ao qual o provedor de recursos personalizado fará a solicitação de proxy. Isso pode ser na forma de um URI simples (por exemplo, ' https://testendpoint/ ') ou pode especificar a rota por meio de um caminho (por exemplo, ' https://testendpoint/{requestPath} ')
  - `Name <String>`: O nome da definição de roteiro. Isso se torna o nome da extensão do braço (por exemplo, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")
  - `[RoutingType <ResourceTypeRouting?>]`: Os tipos de roteamento com suporte para solicitações de recurso.

VALIDATION <ICustomRpValidations [] >: uma lista de validações a serem executadas nas solicitações do provedor de recursos personalizado.
  - `Specification <String>`: Um link para a especificação de validação. A especificação deve ser hospedada no raw.githubusercontent.com.
  - `[ValidationType <ValidationType?>]`: O tipo de validação a ser executada em uma solicitação correspondente.

## LINKS RELACIONADOS

