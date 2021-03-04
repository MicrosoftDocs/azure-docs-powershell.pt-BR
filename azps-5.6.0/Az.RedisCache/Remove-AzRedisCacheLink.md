---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 2227f4fc9cd8128018160a3e62d9ba56bd664d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885522"
---
# <span data-ttu-id="fd615-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fd615-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="fd615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd615-102">SYNOPSIS</span></span>
<span data-ttu-id="fd615-103">Remova um link de replicação geográfica entre dois Caches Redis.</span><span class="sxs-lookup"><span data-stu-id="fd615-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="fd615-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fd615-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd615-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fd615-105">DESCRIPTION</span></span>
<span data-ttu-id="fd615-106">Remova um link de replicação geográfica entre dois Caches Redis.</span><span class="sxs-lookup"><span data-stu-id="fd615-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="fd615-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd615-107">EXAMPLES</span></span>

### <span data-ttu-id="fd615-108">Exemplo 1: Remover um link de replicação geográfica</span><span class="sxs-lookup"><span data-stu-id="fd615-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="fd615-109">Este comando remove links de replicação geográfica em que o Cache Redis denominado mycache1 é primário e o Cache Redis denominado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="fd615-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="fd615-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fd615-110">PARAMETERS</span></span>

### <span data-ttu-id="fd615-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd615-111">-DefaultProfile</span></span>
<span data-ttu-id="fd615-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fd615-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd615-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd615-113">-PassThru</span></span>
<span data-ttu-id="fd615-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fd615-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd615-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="fd615-115">-PrimaryServerName</span></span>
<span data-ttu-id="fd615-116">Nome do cache de redis primário no link.</span><span class="sxs-lookup"><span data-stu-id="fd615-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="fd615-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="fd615-117">-SecondaryServerName</span></span>
<span data-ttu-id="fd615-118">Nome do cache de redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="fd615-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="fd615-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd615-119">-Confirm</span></span>
<span data-ttu-id="fd615-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd615-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd615-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd615-121">-WhatIf</span></span>
<span data-ttu-id="fd615-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd615-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd615-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd615-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd615-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd615-124">CommonParameters</span></span>
<span data-ttu-id="fd615-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd615-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd615-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd615-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd615-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd615-127">INPUTS</span></span>

### <span data-ttu-id="fd615-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fd615-128">System.String</span></span>

## <span data-ttu-id="fd615-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fd615-129">OUTPUTS</span></span>

### <span data-ttu-id="fd615-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd615-130">System.Boolean</span></span>

## <span data-ttu-id="fd615-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="fd615-131">NOTES</span></span>

## <span data-ttu-id="fd615-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd615-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd615-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fd615-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="fd615-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fd615-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="fd615-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd615-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="fd615-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd615-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="fd615-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd615-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="fd615-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd615-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)