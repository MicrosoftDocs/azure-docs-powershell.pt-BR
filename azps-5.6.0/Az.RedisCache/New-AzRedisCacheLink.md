---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 41a2172fffdbd83edc8ab72a4fe922d600362731
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887974"
---
# <span data-ttu-id="761e5-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="761e5-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="761e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="761e5-102">SYNOPSIS</span></span>
<span data-ttu-id="761e5-103">Crie um link de replicação geográfica entre dois Caches Redis.</span><span class="sxs-lookup"><span data-stu-id="761e5-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="761e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="761e5-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="761e5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="761e5-105">DESCRIPTION</span></span>
<span data-ttu-id="761e5-106">Crie um link de replicação geográfica entre dois Caches Redis.</span><span class="sxs-lookup"><span data-stu-id="761e5-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="761e5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="761e5-107">EXAMPLES</span></span>

### <span data-ttu-id="761e5-108">Exemplo 1: Criar um link entre dois caches</span><span class="sxs-lookup"><span data-stu-id="761e5-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="761e5-109">Este comando cria um link de replicação geográfica entre Mycache1 e mycache2 do Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="761e5-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="761e5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="761e5-110">PARAMETERS</span></span>

### <span data-ttu-id="761e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761e5-111">-DefaultProfile</span></span>
<span data-ttu-id="761e5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="761e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="761e5-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="761e5-113">-PrimaryServerName</span></span>
<span data-ttu-id="761e5-114">Nome do cache de redis primário no link.</span><span class="sxs-lookup"><span data-stu-id="761e5-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="761e5-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="761e5-115">-SecondaryServerName</span></span>
<span data-ttu-id="761e5-116">Nome do cache de redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="761e5-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="761e5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="761e5-117">-Confirm</span></span>
<span data-ttu-id="761e5-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="761e5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="761e5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="761e5-119">-WhatIf</span></span>
<span data-ttu-id="761e5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="761e5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="761e5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="761e5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="761e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761e5-122">CommonParameters</span></span>
<span data-ttu-id="761e5-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="761e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761e5-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="761e5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761e5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="761e5-125">INPUTS</span></span>

### <span data-ttu-id="761e5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="761e5-126">System.String</span></span>

## <span data-ttu-id="761e5-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="761e5-127">OUTPUTS</span></span>

### <span data-ttu-id="761e5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="761e5-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="761e5-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="761e5-129">NOTES</span></span>

## <span data-ttu-id="761e5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="761e5-130">RELATED LINKS</span></span>

[<span data-ttu-id="761e5-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="761e5-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="761e5-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="761e5-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="761e5-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="761e5-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="761e5-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="761e5-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="761e5-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="761e5-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="761e5-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="761e5-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)