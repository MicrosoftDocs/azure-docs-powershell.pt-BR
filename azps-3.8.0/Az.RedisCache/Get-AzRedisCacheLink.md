---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943565"
---
# <span data-ttu-id="a40d5-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a40d5-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="a40d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a40d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a40d5-103">Obter link de replicação geográfica para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a40d5-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="a40d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a40d5-104">SYNTAX</span></span>

### <span data-ttu-id="a40d5-105">AllLinksForCache (padrão)</span><span class="sxs-lookup"><span data-stu-id="a40d5-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40d5-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a40d5-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="a40d5-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40d5-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a40d5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a40d5-109">DESCRIPTION</span></span>
<span data-ttu-id="a40d5-110">Há quatro maneiras diferentes de obter detalhes do link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="a40d5-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="a40d5-111">Forneça o nome do parâmetro ou PrimaryServerName e/ou SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="a40d5-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="a40d5-112">O nome é fornecido e, em seguida, todos os links onde o cache existe será retornado.</span><span class="sxs-lookup"><span data-stu-id="a40d5-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="a40d5-113">Se apenas PrimaryServerName for fornecido, todos os links em que o cache é primário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="a40d5-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="a40d5-114">Se apenas SecondaryServerName for fornecido, todos os links em que o cache é secundário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="a40d5-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="a40d5-115">Se PrimaryServerName e SecondaryServerName forem fornecidos, o link específico com função correta será retornado.</span><span class="sxs-lookup"><span data-stu-id="a40d5-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="a40d5-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a40d5-116">EXAMPLES</span></span>

### <span data-ttu-id="a40d5-117">Exemplo 1: obter usando o conjunto de parâmetros AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a40d5-118">Esse comando obtém todos os links de replicação geográfica para o cache Redis chamado myCache1.</span><span class="sxs-lookup"><span data-stu-id="a40d5-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="a40d5-119">Exemplo 2: obter usando o conjunto de parâmetros AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a40d5-120">Esse comando obtém links de replicação geográfica em que o cache do Redis chamado myCache1 é primário.</span><span class="sxs-lookup"><span data-stu-id="a40d5-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="a40d5-121">Exemplo 3: obter usando o conjunto de parâmetros AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a40d5-122">Esse comando obtém links de replicação geográfica em que o cache do Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="a40d5-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="a40d5-123">Exemplo 4: obter usando o conjunto de parâmetros SingleLink</span><span class="sxs-lookup"><span data-stu-id="a40d5-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="a40d5-124">Esse comando obtém um único link de replicação geográfica em que o cache do Redis chamado myCache1 é o cache principal e Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="a40d5-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="a40d5-125">OS</span><span class="sxs-lookup"><span data-stu-id="a40d5-125">PARAMETERS</span></span>

### <span data-ttu-id="a40d5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40d5-126">-DefaultProfile</span></span>
<span data-ttu-id="a40d5-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a40d5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40d5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="a40d5-128">-Name</span></span>
<span data-ttu-id="a40d5-129">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a40d5-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="a40d5-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="a40d5-130">-PrimaryServerName</span></span>
<span data-ttu-id="a40d5-131">Nome do cache principal do Redis no link.</span><span class="sxs-lookup"><span data-stu-id="a40d5-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="a40d5-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="a40d5-132">-SecondaryServerName</span></span>
<span data-ttu-id="a40d5-133">Nome do cache de Redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="a40d5-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="a40d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40d5-134">CommonParameters</span></span>
<span data-ttu-id="a40d5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40d5-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40d5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40d5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a40d5-137">INPUTS</span></span>

### <span data-ttu-id="a40d5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a40d5-138">System.String</span></span>

## <span data-ttu-id="a40d5-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a40d5-139">OUTPUTS</span></span>

### <span data-ttu-id="a40d5-140">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="a40d5-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="a40d5-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a40d5-141">NOTES</span></span>

## <span data-ttu-id="a40d5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a40d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="a40d5-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a40d5-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="a40d5-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a40d5-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="a40d5-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="a40d5-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="a40d5-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a40d5-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a40d5-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)