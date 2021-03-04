---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889172"
---
# <span data-ttu-id="c6f12-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c6f12-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="c6f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f12-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f12-103">Obter link de replicação geográfica para Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="c6f12-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="c6f12-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6f12-104">SYNTAX</span></span>

### <span data-ttu-id="c6f12-105">AllLinksForCache (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6f12-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f12-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f12-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="c6f12-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f12-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6f12-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6f12-109">DESCRIPTION</span></span>
<span data-ttu-id="c6f12-110">Há quatro maneiras diferentes de obter detalhes do link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="c6f12-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="c6f12-111">Forneça Nome do parâmetro ou PrimaryServerName e/ou SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="c6f12-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="c6f12-112">O nome é dado, em seguida, todos os links onde o cache existe serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c6f12-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="c6f12-113">Se somente PrimaryServerName for dado, todos os links onde o cache é principal serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c6f12-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="c6f12-114">Se somente SecondaryServerName for dado, todos os links onde o cache é secundário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c6f12-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="c6f12-115">Se PrimaryServerName e SecondaryServerName ambos são dados, o link específico com a função correta será retornado.</span><span class="sxs-lookup"><span data-stu-id="c6f12-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="c6f12-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6f12-116">EXAMPLES</span></span>

### <span data-ttu-id="c6f12-117">Exemplo 1: Obter o conjunto de parâmetros AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="c6f12-118">Este comando obtém todos os links de replicação geográfica para o Cache Redis chamado mycache1.</span><span class="sxs-lookup"><span data-stu-id="c6f12-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="c6f12-119">Exemplo 2: Obter o conjunto de parâmetros AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="c6f12-120">Este comando obtém links de replicação geográfica onde o Cache redis chamado mycache1 é principal.</span><span class="sxs-lookup"><span data-stu-id="c6f12-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="c6f12-121">Exemplo 3: Obter o conjunto de parâmetros AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="c6f12-122">Este comando obtém links de replicação geográfica onde o Cache redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="c6f12-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="c6f12-123">Exemplo 4: Obter o conjunto de parâmetros SingleLink</span><span class="sxs-lookup"><span data-stu-id="c6f12-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="c6f12-124">Este comando obtém um único link de replicação geográfica em que o Cache Redis denominado mycache1 é principal e o Cache Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="c6f12-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="c6f12-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6f12-125">PARAMETERS</span></span>

### <span data-ttu-id="c6f12-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f12-126">-DefaultProfile</span></span>
<span data-ttu-id="c6f12-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c6f12-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6f12-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c6f12-128">-Name</span></span>
<span data-ttu-id="c6f12-129">Nome do cache redis.</span><span class="sxs-lookup"><span data-stu-id="c6f12-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f12-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="c6f12-130">-PrimaryServerName</span></span>
<span data-ttu-id="c6f12-131">Nome do cache de redis primário no link.</span><span class="sxs-lookup"><span data-stu-id="c6f12-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f12-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="c6f12-132">-SecondaryServerName</span></span>
<span data-ttu-id="c6f12-133">Nome do cache de redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="c6f12-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f12-134">CommonParameters</span></span>
<span data-ttu-id="c6f12-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f12-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f12-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f12-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6f12-137">INPUTS</span></span>

### <span data-ttu-id="c6f12-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f12-138">System.String</span></span>

## <span data-ttu-id="c6f12-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6f12-139">OUTPUTS</span></span>

### <span data-ttu-id="c6f12-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="c6f12-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="c6f12-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6f12-141">NOTES</span></span>

## <span data-ttu-id="c6f12-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6f12-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6f12-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c6f12-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="c6f12-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="c6f12-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="c6f12-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c6f12-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c6f12-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c6f12-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c6f12-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)