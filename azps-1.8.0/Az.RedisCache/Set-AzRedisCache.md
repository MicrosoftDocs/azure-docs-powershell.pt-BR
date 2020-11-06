---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599525"
---
# Set-AzRedisCache

## Sinopse
Modifica um cache Redis.

## SYNTAX

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzRedisCache** modifica um cache do Azure Redis.

## EXEMPLOS

### Exemplo 1: modificar um cache Redis
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.

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

### -EnableNonSslPort
Indica se a porta não SSL está habilitada.
O valor padrão é $False (a porta não SSL está desativada).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do cache do Redis a ser atualizado.

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

### -RedisConfiguration
Especifica as configurações de configuração do Redis.
Os valores aceitáveis para esse parâmetro são:
- RDB-habilitado para backup.
Especifica que a persistência de dados do Redis está habilitada.
Somente camada Premium.
- RDB-Storage-Connection-cadeia de caracteres.
Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.
Somente camada Premium.
- RDB-backup-frequência.
Especifica a frequência de backup para persistência de dados do Redis.
Somente camada Premium. 
- MaxMemory-reservado.
Configura a memória reservada para processos que não são de cache.
Camadas padrão e Premium. 
- MaxMemory-política.
Configura a política de remoção para o cache.
Todas as camadas de preços. 
- Notify-keyspace-Events.
Configura notificações de espaço livre.
Camadas padrão e Premium. 
- hash-Max-ziplist-entradas.
Configura a otimização de memória para tipos de dados de agregação pequenos.
Camadas padrão e Premium. 
- hash-Max-ziplist-Value.
Configura a otimização de memória para tipos de dados de agregação pequenos.
Camadas padrão e Premium. 
- SET-Max-intset-entradas.
Configura a otimização de memória para tipos de dados de agregação pequenos.
Camadas padrão e Premium. 
- zset-Max-ziplist-Entries.
Configura a otimização de memória para tipos de dados de agregação pequenos.
Camadas padrão e Premium. 
- zset-Max-ziplist-Value.
Configura a otimização de memória para tipos de dados de agregação pequenos.
Camadas padrão e Premium. 
- bancos.
Configura o número de bancos de dados.
Essa propriedade pode ser configurada somente na criação do cache.
Camadas padrão e Premium.
Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém o cache Redis.

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

### -ShardCount
Especifica o número de fragmentos a serem criados em um cache de cluster Premium.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tamanho
Especifica o tamanho do cache Redis.
Os valores válidos são: 
- P1
- P2
- P3
- P4
- C0
- C1
- C2
- C3
- C4
- C5
- C6
- 250MB
- 1 GB
- 2,5 GB
- 6GB
- 13GB
- 26GB
- 53GB o valor padrão é 1GB ou C1.

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

### -SKU
Especifica o SKU do cache Redis a ser criado.
Os valores válidos são: 
- Basic
- Oficial
- Premium o valor padrão é padrão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Uma tabela de hash que representa as marcas.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Esse parâmetro foi preterido.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. Collections. Hashtable

### System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## EXIBE

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys

## INFORMA

## LINKS RELACIONADOS

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)


