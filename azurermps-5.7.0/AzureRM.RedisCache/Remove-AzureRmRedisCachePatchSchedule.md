---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432418"
---
# <span data-ttu-id="5a593-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5a593-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="5a593-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a593-102">SYNOPSIS</span></span>
<span data-ttu-id="5a593-103">Remove o cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="5a593-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a593-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a593-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a593-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a593-105">DESCRIPTION</span></span>
<span data-ttu-id="5a593-106">O cmdlet **Remove-AzureRmRedisCachePatchSchedule** remove o cronograma do patch de um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="5a593-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="5a593-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a593-107">EXAMPLES</span></span>

### <span data-ttu-id="5a593-108">Exemplo 1: remover o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="5a593-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="5a593-109">Esse comando Remove o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="5a593-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="5a593-110">OS</span><span class="sxs-lookup"><span data-stu-id="5a593-110">PARAMETERS</span></span>

### <span data-ttu-id="5a593-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a593-111">-DefaultProfile</span></span>
<span data-ttu-id="5a593-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5a593-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a593-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a593-113">-Name</span></span>
<span data-ttu-id="5a593-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="5a593-114">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a593-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a593-115">-PassThru</span></span>
<span data-ttu-id="5a593-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="5a593-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a593-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a593-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a593-118">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="5a593-118">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a593-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5a593-119">-Confirm</span></span>
<span data-ttu-id="5a593-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a593-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a593-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a593-121">-WhatIf</span></span>
<span data-ttu-id="5a593-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a593-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a593-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a593-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a593-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a593-124">CommonParameters</span></span>
<span data-ttu-id="5a593-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a593-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a593-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a593-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a593-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a593-127">INPUTS</span></span>

### <span data-ttu-id="5a593-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5a593-128">None</span></span>
<span data-ttu-id="5a593-129">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="5a593-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5a593-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a593-130">OUTPUTS</span></span>

### <span data-ttu-id="5a593-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5a593-131">None</span></span>

## <span data-ttu-id="5a593-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a593-132">NOTES</span></span>
* <span data-ttu-id="5a593-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="5a593-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5a593-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a593-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a593-135">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5a593-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="5a593-136">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="5a593-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="5a593-137">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="5a593-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


