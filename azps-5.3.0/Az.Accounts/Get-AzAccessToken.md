---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432833"
---
# Get-AzAccessToken

## Sinopse
Obter token de acesso bruto. Ao usar-ResourceUrl, certifique-se de que o valor corresponda ao ambiente atual do Azure. Você pode se referir ao valor de `(Get-AzContext).Environment` .

## SYNTAX

### KnownResourceTypeName (padrão)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
Obter token de acesso

## EXEMPLOS

### Exemplo 1 obter token de acesso bruto para o ponto de extremidade do ARM
```powershell
PS C:\> Get-AzAccessToken
```

Obter o token de acesso do ponto de extremidade ResourceManager para a conta atual

### Exemplo 2 obter token de acesso bruto para o ponto de extremidade do AAD Graph
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Obter o token de acesso do ponto de extremidade do AAD Graph para a conta atual

### Exemplo 3 obter token de acesso bruto para o ponto de extremidade do AAD Graph
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Obter o token de acesso do ponto de extremidade do AAD Graph para a conta atual

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -ResourceTypename
Nome do tipo de recurso opcional, valores com suporte: AadGraph, AnalysisServices, ARM, atestado, Batch, datalake, keyvault, OperationalInsights, ResourceManager, Synapse. O valor padrão é ARM se não for especificado.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
URL do recurso para o qual você está solicitando o token, por exemplo, ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantid
ID de locatário opcional. Use a ID de locatário do contexto padrão, se não especificado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS
