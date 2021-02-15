---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111451"
---
# <span data-ttu-id="d974e-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d974e-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d974e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d974e-102">SYNOPSIS</span></span>
<span data-ttu-id="d974e-103">Obtém um cronograma de patch.</span><span class="sxs-lookup"><span data-stu-id="d974e-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="d974e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d974e-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d974e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d974e-105">DESCRIPTION</span></span>
<span data-ttu-id="d974e-106">O cmdlet **Get-AzRedisCachePatchSchedule obtém** um cronograma de patch para um cache no Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d974e-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d974e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d974e-107">EXAMPLES</span></span>

### <span data-ttu-id="d974e-108">Exemplo 1: Obter o cronograma de patch</span><span class="sxs-lookup"><span data-stu-id="d974e-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="d974e-109">Esse comando obtém o cronograma de patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="d974e-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="d974e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d974e-110">PARAMETERS</span></span>

### <span data-ttu-id="d974e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d974e-111">-DefaultProfile</span></span>
<span data-ttu-id="d974e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d974e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d974e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d974e-113">-Name</span></span>
<span data-ttu-id="d974e-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="d974e-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="d974e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d974e-115">-ResourceGroupName</span></span>
<span data-ttu-id="d974e-116">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="d974e-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d974e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d974e-117">CommonParameters</span></span>
<span data-ttu-id="d974e-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d974e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d974e-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d974e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d974e-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="d974e-120">INPUTS</span></span>

### <span data-ttu-id="d974e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d974e-121">System.String</span></span>

## <span data-ttu-id="d974e-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="d974e-122">OUTPUTS</span></span>

### <span data-ttu-id="d974e-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d974e-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="d974e-124">Notas</span><span class="sxs-lookup"><span data-stu-id="d974e-124">NOTES</span></span>
* <span data-ttu-id="d974e-125">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="d974e-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d974e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d974e-126">RELATED LINKS</span></span>

[<span data-ttu-id="d974e-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d974e-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="d974e-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d974e-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="d974e-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d974e-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


