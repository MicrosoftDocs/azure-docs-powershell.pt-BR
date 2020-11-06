---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427805"
---
# <span data-ttu-id="94349-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="94349-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="94349-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94349-102">SYNOPSIS</span></span>
<span data-ttu-id="94349-103">Remove o cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="94349-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94349-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94349-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94349-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94349-105">DESCRIPTION</span></span>
<span data-ttu-id="94349-106">O cmdlet **Remove-AzureRmRedisCachePatchSchedule** remove o cronograma do patch de um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="94349-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="94349-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94349-107">EXAMPLES</span></span>

### <span data-ttu-id="94349-108">Exemplo 1: remover o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="94349-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="94349-109">Esse comando Remove o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="94349-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="94349-110">OS</span><span class="sxs-lookup"><span data-stu-id="94349-110">PARAMETERS</span></span>

### <span data-ttu-id="94349-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="94349-111">-Name</span></span>
<span data-ttu-id="94349-112">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="94349-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="94349-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94349-113">-ResourceGroupName</span></span>
<span data-ttu-id="94349-114">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="94349-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="94349-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94349-115">-Confirm</span></span>
<span data-ttu-id="94349-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94349-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94349-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94349-117">-WhatIf</span></span>
<span data-ttu-id="94349-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94349-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94349-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94349-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94349-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94349-120">-DefaultProfile</span></span>
<span data-ttu-id="94349-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94349-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94349-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94349-122">CommonParameters</span></span>
<span data-ttu-id="94349-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94349-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94349-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94349-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94349-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94349-125">INPUTS</span></span>

### <span data-ttu-id="94349-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="94349-126">None</span></span>
<span data-ttu-id="94349-127">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="94349-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="94349-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94349-128">OUTPUTS</span></span>

### <span data-ttu-id="94349-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="94349-129">None</span></span>

## <span data-ttu-id="94349-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94349-130">NOTES</span></span>
* <span data-ttu-id="94349-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="94349-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="94349-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94349-132">RELATED LINKS</span></span>

[<span data-ttu-id="94349-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="94349-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="94349-134">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="94349-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="94349-135">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="94349-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


