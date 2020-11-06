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
# <span data-ttu-id="35950-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="35950-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="35950-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35950-102">SYNOPSIS</span></span>
<span data-ttu-id="35950-103">Obter link de replicação geográfica para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="35950-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35950-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35950-104">SYNTAX</span></span>

### <span data-ttu-id="35950-105">AllLinksForCache (padrão)</span><span class="sxs-lookup"><span data-stu-id="35950-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35950-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="35950-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35950-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="35950-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35950-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="35950-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35950-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35950-109">DESCRIPTION</span></span>
<span data-ttu-id="35950-110">Há quatro maneiras diferentes de obter detalhes do link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="35950-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="35950-111">Forneça o nome do parâmetro ou PrimaryServerName e/ou SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="35950-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="35950-112">O nome é fornecido e, em seguida, todos os links onde o cache existe será retornado.</span><span class="sxs-lookup"><span data-stu-id="35950-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="35950-113">Se apenas PrimaryServerName for fornecido, todos os links em que o cache é primário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="35950-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="35950-114">Se apenas SecondaryServerName for fornecido, todos os links em que o cache é secundário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="35950-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="35950-115">Se PrimaryServerName e SecondaryServerName forem fornecidos, o link específico com função correta será retornado.</span><span class="sxs-lookup"><span data-stu-id="35950-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="35950-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35950-116">EXAMPLES</span></span>

### <span data-ttu-id="35950-117">Exemplo 1: obter usando o conjunto de parâmetros AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="35950-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="35950-118">Esse comando obtém todos os links de replicação geográfica para o cache Redis chamado myCache1.</span><span class="sxs-lookup"><span data-stu-id="35950-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="35950-119">Exemplo 2: obter usando o conjunto de parâmetros AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="35950-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="35950-120">Esse comando obtém links de replicação geográfica em que o cache do Redis chamado myCache1 é primário.</span><span class="sxs-lookup"><span data-stu-id="35950-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="35950-121">Exemplo 3: obter usando o conjunto de parâmetros AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="35950-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="35950-122">Esse comando obtém links de replicação geográfica em que o cache do Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="35950-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="35950-123">Exemplo 4: obter usando o conjunto de parâmetros SingleLink</span><span class="sxs-lookup"><span data-stu-id="35950-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="35950-124">Esse comando obtém um único link de replicação geográfica em que o cache do Redis chamado myCache1 é o cache principal e Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="35950-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="35950-125">OS</span><span class="sxs-lookup"><span data-stu-id="35950-125">PARAMETERS</span></span>

### <span data-ttu-id="35950-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35950-126">-DefaultProfile</span></span>
<span data-ttu-id="35950-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35950-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35950-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="35950-128">-Name</span></span>
<span data-ttu-id="35950-129">Nome do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="35950-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="35950-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="35950-130">-PrimaryServerName</span></span>
<span data-ttu-id="35950-131">Nome do cache principal do Redis no link.</span><span class="sxs-lookup"><span data-stu-id="35950-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="35950-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="35950-132">-SecondaryServerName</span></span>
<span data-ttu-id="35950-133">Nome do cache de Redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="35950-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="35950-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35950-134">CommonParameters</span></span>
<span data-ttu-id="35950-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35950-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35950-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35950-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35950-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35950-137">INPUTS</span></span>

### <span data-ttu-id="35950-138">System. String</span><span class="sxs-lookup"><span data-stu-id="35950-138">System.String</span></span>
<span data-ttu-id="35950-139">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="35950-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="35950-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35950-140">OUTPUTS</span></span>

### <span data-ttu-id="35950-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="35950-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="35950-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35950-142">NOTES</span></span>

## <span data-ttu-id="35950-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35950-143">RELATED LINKS</span></span>

[<span data-ttu-id="35950-144">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="35950-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="35950-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="35950-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="35950-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35950-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="35950-147">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35950-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="35950-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35950-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="35950-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="35950-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
