---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428817"
---
# New-AzureRmRedisCache

## Sinopse
Cria um cache Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmRedisCache** cria um cache do Azure Redis.

## EXEMPLOS

### Exemplo 1: criar um cache Redis
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Esse comando cria um cache Redis.

### Exemplo 2: criar um cache de Redis de SKU padrão
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

Esse comando cria um cache Redis.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o local no qual criar um cache Redis.
Os valores válidos são: 

- Centro Norte dos EUA
- Centro-Sul dos EUA
- Centro dos EUA
- Oeste da Europa
- Norte da Europa
- Oeste dos EUA
- Leste dos EUA
- Leste dos EUA 2
- Japão oriental
- Oeste do Japão
- Sul do Brasil
- Sudeste Asiático
- Leste da Ásia
- Leste da Austrália
- Sudeste da Austrália

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do cache de Redis a ser criado.

```yaml
Type: String
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
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisVersion
Esse parâmetro é preterido e será removido de versões futuras.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos no qual criar o cache Redis.

```yaml
Type: String
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
Os valores aceitáveis para esse parâmetro são:

- um
- 2
- 3D
- 4
- 5
- 5
- 7
- 08
- 222 
- 254

```yaml
Type: Int32
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticIP
Especifica um endereço IP exclusivo na sub-rede para o cache Redis.

Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnet
Especifica o nome da sub-rede na qual implantar o cache Redis.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnetid
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Uma tabela de hash que representa as marcas.

```yaml
Type: Hashtable
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
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Especifica a ID do recurso da rede virtual na qual você deseja implantar o cache Redis.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Lista de zonas.

```yaml
Type: String[]
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.

## EXIBE

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Esse cmdlet retorna todos os atributos de um cache Redis incluindo as chaves de acesso primária e secundária.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


