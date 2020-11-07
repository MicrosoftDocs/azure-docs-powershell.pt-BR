---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778185"
---
# <span data-ttu-id="f63ae-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f63ae-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f63ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f63ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f63ae-103">Remove o cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="f63ae-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="f63ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f63ae-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f63ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f63ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f63ae-106">O cmdlet **Remove-AzRedisCachePatchSchedule** remove o cronograma do patch de um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="f63ae-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f63ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f63ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f63ae-108">Exemplo 1: remover o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="f63ae-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="f63ae-109">Esse comando Remove o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="f63ae-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="f63ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="f63ae-110">PARAMETERS</span></span>

### <span data-ttu-id="f63ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63ae-111">-DefaultProfile</span></span>
<span data-ttu-id="f63ae-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f63ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f63ae-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f63ae-113">-Name</span></span>
<span data-ttu-id="f63ae-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="f63ae-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f63ae-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f63ae-115">-PassThru</span></span>
<span data-ttu-id="f63ae-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="f63ae-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f63ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f63ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="f63ae-118">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="f63ae-118">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f63ae-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f63ae-119">-Confirm</span></span>
<span data-ttu-id="f63ae-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f63ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f63ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f63ae-121">-WhatIf</span></span>
<span data-ttu-id="f63ae-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f63ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f63ae-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f63ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f63ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63ae-124">CommonParameters</span></span>
<span data-ttu-id="f63ae-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f63ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63ae-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63ae-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f63ae-127">INPUTS</span></span>

### <span data-ttu-id="f63ae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f63ae-128">System.String</span></span>

## <span data-ttu-id="f63ae-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f63ae-129">OUTPUTS</span></span>

### <span data-ttu-id="f63ae-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f63ae-130">System.Boolean</span></span>

## <span data-ttu-id="f63ae-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f63ae-131">NOTES</span></span>
* <span data-ttu-id="f63ae-132">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="f63ae-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f63ae-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f63ae-133">RELATED LINKS</span></span>

[<span data-ttu-id="f63ae-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f63ae-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f63ae-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f63ae-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f63ae-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f63ae-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


