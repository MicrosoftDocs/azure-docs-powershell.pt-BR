---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115573"
---
# Get-AzAccessToken

## Sinopse
Obter token de acesso bruto. Ao usar -ResourceUrl, verifique se o valor é igual ao ambiente atual do Azure. Você pode se referir ao valor de `(Get-AzContext).Environment` .

## Sintaxe

### KnownResourceTypeName (Padrão)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
Obter token de acesso

## Exemplos

### Exemplo 1 Obter token de acesso bruto para o ponto de extremidade ARM
```powershell
PS C:\> Get-AzAccessToken
```

Obter token de acesso do ponto de extremidade ResourceManager para a conta atual

### Exemplo 2 Obter token de acesso bruto para o ponto de extremidade do AAD Graph
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Obter token de acesso do ponto de extremidade do gráfico AAD para a conta atual

### Exemplo 3 Obter token de acesso bruto para o ponto de extremidade do AAD Graph
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Obter token de acesso do ponto de extremidade do gráfico AAD para a conta atual

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -ResourceTypeName
Nome do tipo resouce opcional, valores com suporte: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. O valor padrão é Arm, se não especificado.

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
URL do recurso para o que você está solicitando token, por exemplo' http://graph.windows.net/ '.

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

### -TenantId
ID do Locatário Opcional. Use a ID do locatário do contexto padrão, se não especificada.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### System.String

## Notas

## LINKS RELACIONADOS
