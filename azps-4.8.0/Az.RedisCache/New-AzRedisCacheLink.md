---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111005"
---
# <span data-ttu-id="02175-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02175-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="02175-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02175-102">SYNOPSIS</span></span>
<span data-ttu-id="02175-103">Crie um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="02175-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="02175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02175-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02175-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02175-105">DESCRIPTION</span></span>
<span data-ttu-id="02175-106">Crie um link de replicação geográfica entre dois caches do Redis.</span><span class="sxs-lookup"><span data-stu-id="02175-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="02175-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02175-107">EXAMPLES</span></span>

### <span data-ttu-id="02175-108">Exemplo 1: criar um link entre dois caches</span><span class="sxs-lookup"><span data-stu-id="02175-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="02175-109">Esse comando cria um link de replicação geográfica entre o Redis cache myCache1 e o mycache2.</span><span class="sxs-lookup"><span data-stu-id="02175-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="02175-110">OS</span><span class="sxs-lookup"><span data-stu-id="02175-110">PARAMETERS</span></span>

### <span data-ttu-id="02175-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02175-111">-DefaultProfile</span></span>
<span data-ttu-id="02175-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02175-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02175-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="02175-113">-PrimaryServerName</span></span>
<span data-ttu-id="02175-114">Nome do cache principal do Redis no link.</span><span class="sxs-lookup"><span data-stu-id="02175-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="02175-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="02175-115">-SecondaryServerName</span></span>
<span data-ttu-id="02175-116">Nome do cache de Redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="02175-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="02175-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02175-117">-Confirm</span></span>
<span data-ttu-id="02175-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02175-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02175-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02175-119">-WhatIf</span></span>
<span data-ttu-id="02175-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02175-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02175-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02175-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02175-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02175-122">CommonParameters</span></span>
<span data-ttu-id="02175-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02175-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02175-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02175-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02175-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02175-125">INPUTS</span></span>

### <span data-ttu-id="02175-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02175-126">System.String</span></span>

## <span data-ttu-id="02175-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02175-127">OUTPUTS</span></span>

### <span data-ttu-id="02175-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="02175-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="02175-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02175-129">NOTES</span></span>

## <span data-ttu-id="02175-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02175-130">RELATED LINKS</span></span>

[<span data-ttu-id="02175-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02175-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="02175-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="02175-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="02175-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02175-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="02175-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02175-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="02175-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02175-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="02175-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="02175-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)