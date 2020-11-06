---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428819"
---
# Get-AzureRmRedisCacheLink

## Sinopse
Obter link de replicação geográfica para o cache Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### AllLinksForCache (padrão)
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
Há quatro maneiras diferentes de obter detalhes do link de replicação geográfica. Forneça o nome do parâmetro ou PrimaryServerName e/ou SecondaryServerName. O nome é fornecido e, em seguida, todos os links onde o cache existe será retornado. Se apenas PrimaryServerName for fornecido, todos os links em que o cache é primário serão retornados. Se apenas SecondaryServerName for fornecido, todos os links em que o cache é secundário serão retornados. Se PrimaryServerName e SecondaryServerName forem fornecidos, o link específico com função correta será retornado. 

## EXEMPLOS

### Exemplo 1: obter usando o conjunto de parâmetros AllLinksForCache
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Esse comando obtém todos os links de replicação geográfica para o cache Redis chamado myCache1.

### Exemplo 2: obter usando o conjunto de parâmetros AllLinksForPrimaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Esse comando obtém links de replicação geográfica em que o cache do Redis chamado myCache1 é primário.

### Exemplo 3: obter usando o conjunto de parâmetros AllLinksForSecondaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Esse comando obtém links de replicação geográfica em que o cache do Redis chamado mycache2 é secundário.

### Exemplo 4: obter usando o conjunto de parâmetros SingleLink
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Esse comando obtém um único link de replicação geográfica em que o cache do Redis chamado myCache1 é o cache principal e Redis chamado mycache2 é secundário.

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

### -Nome
Nome do cache Redis.

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Nome do cache principal do Redis no link.

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Nome do cache de Redis secundário no link.

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String
Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.

## EXIBE

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmRedisCacheLink](./New-AzureRmRedisCacheLink.md)

[Remove-AzureRmRedisCacheLink](./Remove-AzureRmRedisCacheLink.md)

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)
