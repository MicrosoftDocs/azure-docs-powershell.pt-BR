---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114026"
---
# <span data-ttu-id="4de2e-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4de2e-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="4de2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4de2e-102">SYNOPSIS</span></span>
<span data-ttu-id="4de2e-103">Obter link de replicação geográfica para o Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="4de2e-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="4de2e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4de2e-104">SYNTAX</span></span>

### <span data-ttu-id="4de2e-105">AllLinksForCache (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4de2e-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4de2e-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4de2e-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="4de2e-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4de2e-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4de2e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4de2e-109">DESCRIPTION</span></span>
<span data-ttu-id="4de2e-110">Há quatro maneiras diferentes de obter detalhes do link de replicação geográfica.</span><span class="sxs-lookup"><span data-stu-id="4de2e-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="4de2e-111">Forneça Nome do parâmetro ou NomeDoServer Primário e/ou NomeDoServer Secundário.</span><span class="sxs-lookup"><span data-stu-id="4de2e-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="4de2e-112">O nome é dado e, em seguida, todos os links onde o cache existe serão retornados.</span><span class="sxs-lookup"><span data-stu-id="4de2e-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="4de2e-113">Se apenas o PrimaryServerName for dado, todos os links onde o cache é principal serão retornados.</span><span class="sxs-lookup"><span data-stu-id="4de2e-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="4de2e-114">Se apenas o NomeDoServidor Secundário for dado, todos os links em que o cache é secundário serão retornados.</span><span class="sxs-lookup"><span data-stu-id="4de2e-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="4de2e-115">Se PrimaryServerName e SecondaryServerName ambos receberem um link específico com a função correta será retornado.</span><span class="sxs-lookup"><span data-stu-id="4de2e-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="4de2e-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4de2e-116">EXAMPLES</span></span>

### <span data-ttu-id="4de2e-117">Exemplo 1: Usar o conjunto de parâmetros AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="4de2e-118">Esse comando obtém todos os links de replicação geográfica do Cache Redis chamados mycache1.</span><span class="sxs-lookup"><span data-stu-id="4de2e-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="4de2e-119">Exemplo 2: Usar conjunto de parâmetros AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="4de2e-120">Esse comando obtém links de replicação geográfica onde o Cache Redis chamado mycache1 é principal.</span><span class="sxs-lookup"><span data-stu-id="4de2e-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="4de2e-121">Exemplo 3: Usar o conjunto de parâmetros AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="4de2e-122">Esse comando obtém links de replicação geográfica onde o Cache Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="4de2e-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="4de2e-123">Exemplo 4: Usar o conjunto de parâmetros SingleLink</span><span class="sxs-lookup"><span data-stu-id="4de2e-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="4de2e-124">Esse comando obtém um único vínculo de replicação geográfica em que o Cache Redis chamado mycache1 é principal e o Cache Redis chamado mycache2 é secundário.</span><span class="sxs-lookup"><span data-stu-id="4de2e-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="4de2e-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4de2e-125">PARAMETERS</span></span>

### <span data-ttu-id="4de2e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de2e-126">-DefaultProfile</span></span>
<span data-ttu-id="4de2e-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4de2e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de2e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4de2e-128">-Name</span></span>
<span data-ttu-id="4de2e-129">Nome do cache de redis.</span><span class="sxs-lookup"><span data-stu-id="4de2e-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="4de2e-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="4de2e-130">-PrimaryServerName</span></span>
<span data-ttu-id="4de2e-131">Nome do cache de redis primário no link.</span><span class="sxs-lookup"><span data-stu-id="4de2e-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="4de2e-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="4de2e-132">-SecondaryServerName</span></span>
<span data-ttu-id="4de2e-133">Nome do cache de redis secundário no link.</span><span class="sxs-lookup"><span data-stu-id="4de2e-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="4de2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de2e-134">CommonParameters</span></span>
<span data-ttu-id="4de2e-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de2e-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de2e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de2e-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="4de2e-137">INPUTS</span></span>

### <span data-ttu-id="4de2e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4de2e-138">System.String</span></span>

## <span data-ttu-id="4de2e-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="4de2e-139">OUTPUTS</span></span>

### <span data-ttu-id="4de2e-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="4de2e-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="4de2e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="4de2e-141">NOTES</span></span>

## <span data-ttu-id="4de2e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de2e-142">RELATED LINKS</span></span>

[<span data-ttu-id="4de2e-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4de2e-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="4de2e-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="4de2e-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="4de2e-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4de2e-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4de2e-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4de2e-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4de2e-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)