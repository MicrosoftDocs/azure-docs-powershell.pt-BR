---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: a0532feb24966cfe05b0175080fa2333307f33e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429711"
---
# <span data-ttu-id="5e0c6-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5e0c6-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="5e0c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0c6-103">Remover um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e0c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e0c6-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0c6-106">Remover um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="5e0c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="5e0c6-108">Exemplo 1: remover um link de replicação geográfica</span><span class="sxs-lookup"><span data-stu-id="5e0c6-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="5e0c6-109">Esse comando Remove links de replicação geográfica em que o cache do Redis chamado myCache1 é primário e Redis cache chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="5e0c6-110">OS</span><span class="sxs-lookup"><span data-stu-id="5e0c6-110">PARAMETERS</span></span>

### <span data-ttu-id="5e0c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0c6-111">-DefaultProfile</span></span>
<span data-ttu-id="5e0c6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e0c6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e0c6-113">-PassThru</span></span>
<span data-ttu-id="5e0c6-114">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="5e0c6-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0c6-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="5e0c6-115">-PrimaryServerName</span></span>
<span data-ttu-id="5e0c6-116">Nome do cache principal do Redis no link.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="5e0c6-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="5e0c6-117">-SecondaryServerName</span></span>
<span data-ttu-id="5e0c6-118">Nome do cache de Redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="5e0c6-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e0c6-119">-Confirm</span></span>
<span data-ttu-id="5e0c6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0c6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0c6-121">-WhatIf</span></span>
<span data-ttu-id="5e0c6-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0c6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0c6-124">CommonParameters</span></span>
<span data-ttu-id="5e0c6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0c6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0c6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e0c6-127">INPUTS</span></span>

### <span data-ttu-id="5e0c6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5e0c6-128">System.String</span></span>

## <span data-ttu-id="5e0c6-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e0c6-129">OUTPUTS</span></span>

### <span data-ttu-id="5e0c6-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e0c6-130">System.Boolean</span></span>

## <span data-ttu-id="5e0c6-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e0c6-131">NOTES</span></span>

## <span data-ttu-id="5e0c6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e0c6-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e0c6-133">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5e0c6-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="5e0c6-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="5e0c6-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="5e0c6-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5e0c6-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="5e0c6-136">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5e0c6-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="5e0c6-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5e0c6-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="5e0c6-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5e0c6-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)