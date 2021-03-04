---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892734"
---
# <span data-ttu-id="96f45-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="96f45-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="96f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96f45-102">SYNOPSIS</span></span>
<span data-ttu-id="96f45-103">Obtém um cronograma de patch.</span><span class="sxs-lookup"><span data-stu-id="96f45-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="96f45-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96f45-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96f45-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96f45-105">DESCRIPTION</span></span>
<span data-ttu-id="96f45-106">O cmdlet **Get-AzRedisCachePatchSchedule** obtém um cronograma de patch para um cache no Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="96f45-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="96f45-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96f45-107">EXAMPLES</span></span>

### <span data-ttu-id="96f45-108">Exemplo 1: Obter o agendamento de patch</span><span class="sxs-lookup"><span data-stu-id="96f45-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="96f45-109">Este comando obtém o cronograma de patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="96f45-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="96f45-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96f45-110">PARAMETERS</span></span>

### <span data-ttu-id="96f45-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f45-111">-DefaultProfile</span></span>
<span data-ttu-id="96f45-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="96f45-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96f45-113">-Name</span><span class="sxs-lookup"><span data-stu-id="96f45-113">-Name</span></span>
<span data-ttu-id="96f45-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="96f45-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="96f45-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f45-115">-ResourceGroupName</span></span>
<span data-ttu-id="96f45-116">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="96f45-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="96f45-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f45-117">CommonParameters</span></span>
<span data-ttu-id="96f45-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f45-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f45-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f45-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f45-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96f45-120">INPUTS</span></span>

### <span data-ttu-id="96f45-121">System.String</span><span class="sxs-lookup"><span data-stu-id="96f45-121">System.String</span></span>

## <span data-ttu-id="96f45-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96f45-122">OUTPUTS</span></span>

### <span data-ttu-id="96f45-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="96f45-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="96f45-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="96f45-124">NOTES</span></span>
* <span data-ttu-id="96f45-125">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="96f45-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="96f45-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96f45-126">RELATED LINKS</span></span>

[<span data-ttu-id="96f45-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="96f45-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="96f45-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="96f45-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="96f45-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="96f45-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


