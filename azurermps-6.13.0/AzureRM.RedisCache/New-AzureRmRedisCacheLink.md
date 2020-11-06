---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: f625c9180287166b01607c468c44b5e0623c11cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426294"
---
# <span data-ttu-id="921f9-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="921f9-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="921f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="921f9-102">SYNOPSIS</span></span>
<span data-ttu-id="921f9-103">Crie um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="921f9-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="921f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="921f9-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="921f9-105">DESCRIPTION</span></span>
<span data-ttu-id="921f9-106">Crie um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="921f9-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="921f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="921f9-107">EXAMPLES</span></span>

### <span data-ttu-id="921f9-108">Exemplo 1: criar um link entre dois caches</span><span class="sxs-lookup"><span data-stu-id="921f9-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="921f9-109">Esse comando cria um link de replicação geográfica entre o Redis cache myCache1 e o mycache2.</span><span class="sxs-lookup"><span data-stu-id="921f9-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="921f9-110">OS</span><span class="sxs-lookup"><span data-stu-id="921f9-110">PARAMETERS</span></span>

### <span data-ttu-id="921f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921f9-111">-DefaultProfile</span></span>
<span data-ttu-id="921f9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="921f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="921f9-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="921f9-113">-PrimaryServerName</span></span>
<span data-ttu-id="921f9-114">Nome do cache principal do Redis no link.</span><span class="sxs-lookup"><span data-stu-id="921f9-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="921f9-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="921f9-115">-SecondaryServerName</span></span>
<span data-ttu-id="921f9-116">Nome do cache de Redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="921f9-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="921f9-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="921f9-117">-Confirm</span></span>
<span data-ttu-id="921f9-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="921f9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921f9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921f9-119">-WhatIf</span></span>
<span data-ttu-id="921f9-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="921f9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921f9-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="921f9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921f9-122">CommonParameters</span></span>
<span data-ttu-id="921f9-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921f9-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="921f9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921f9-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="921f9-125">INPUTS</span></span>

### <span data-ttu-id="921f9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="921f9-126">System.String</span></span>

## <span data-ttu-id="921f9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="921f9-127">OUTPUTS</span></span>

### <span data-ttu-id="921f9-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="921f9-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="921f9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="921f9-129">NOTES</span></span>

## <span data-ttu-id="921f9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="921f9-130">RELATED LINKS</span></span>

[<span data-ttu-id="921f9-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="921f9-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="921f9-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="921f9-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="921f9-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="921f9-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="921f9-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="921f9-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="921f9-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="921f9-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="921f9-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="921f9-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
