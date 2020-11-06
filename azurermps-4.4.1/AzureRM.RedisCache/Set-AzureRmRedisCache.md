---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429143"
---
# Set-AzureRmRedisCache

## Sinopse
Modifica um cache Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmRedisCache** modifica um cache do Azure Redis.

## EXEMPLOS

### Exemplo 1: modificar um cache Redis
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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
```

Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.

## OS

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

### -MaxMemoryPolicy
Esse parâmetro foi preterido.
Use o parâmetro *RedisConfiguration* para definir MaxMemory-política.
Por exemplo: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

Required: True
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
- 53GB

O valor padrão é 1GB ou C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

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
- Gratifica

O valor padrão é padrão.

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

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Retorna todos os atributos de um cache Redis, incluindo as chaves de acesso primária e secundária.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)


