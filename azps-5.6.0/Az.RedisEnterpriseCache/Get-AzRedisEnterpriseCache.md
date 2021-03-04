---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: fd127005107586e31798d215d7f54888b26705c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891756"
---
# Get-AzRedisEnterpriseCache

## SYNOPSIS
Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado

## SINTAXE

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Obtém informações sobre um cluster RedisEnterprise e seu banco de dados associado

## EXEMPLOS

### Exemplo 1: Obter um Cache da Empresa Redis pelo nome
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

Este comando obtém o Cache da Empresa Redis chamado MyCache.

### Exemplo 2: Obter todos os Redis Enterprise Cache em um grupo de recursos
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

Este comando obtém todos os Redis Enterprise Cache no grupo de recursos especificado.

## PARÂMETROS

### -ClusterName
O nome do cluster RedisEnterprise.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -SubscriptionId
Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster

## NOTES

ALIASES

## LINKS RELACIONADOS

