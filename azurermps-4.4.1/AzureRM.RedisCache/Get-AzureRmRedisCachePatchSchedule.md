---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 1899a35f183f66fb938abe0c6492e826ad661e43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440968"
---
# <span data-ttu-id="31e27-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31e27-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="31e27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31e27-102">SYNOPSIS</span></span>
<span data-ttu-id="31e27-103">Obtém um cronograma de correção.</span><span class="sxs-lookup"><span data-stu-id="31e27-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31e27-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31e27-105">DESCRIPTION</span></span>
<span data-ttu-id="31e27-106">O cmdlet **Get-AzureRmRedisCachePatchSchedule** Obtém um cronograma de patch para um cache no Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="31e27-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="31e27-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31e27-107">EXAMPLES</span></span>

### <span data-ttu-id="31e27-108">Exemplo 1: obter o cronograma do patch</span><span class="sxs-lookup"><span data-stu-id="31e27-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="31e27-109">Esse comando obtém o cronograma do patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="31e27-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="31e27-110">OS</span><span class="sxs-lookup"><span data-stu-id="31e27-110">PARAMETERS</span></span>

### <span data-ttu-id="31e27-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="31e27-111">-Name</span></span>
<span data-ttu-id="31e27-112">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="31e27-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="31e27-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e27-113">-ResourceGroupName</span></span>
<span data-ttu-id="31e27-114">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="31e27-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="31e27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e27-115">-DefaultProfile</span></span>
<span data-ttu-id="31e27-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31e27-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e27-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e27-117">CommonParameters</span></span>
<span data-ttu-id="31e27-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e27-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e27-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e27-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e27-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31e27-120">INPUTS</span></span>

### <span data-ttu-id="31e27-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="31e27-121">None</span></span>
<span data-ttu-id="31e27-122">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="31e27-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="31e27-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31e27-123">OUTPUTS</span></span>

### <span data-ttu-id="31e27-124">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31e27-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="31e27-125">Esse cmdlet retorna as entradas de agendamento de patch definidas no cache.</span><span class="sxs-lookup"><span data-stu-id="31e27-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="31e27-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31e27-126">NOTES</span></span>
* <span data-ttu-id="31e27-127">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="31e27-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="31e27-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31e27-128">RELATED LINKS</span></span>

[<span data-ttu-id="31e27-129">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31e27-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="31e27-130">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="31e27-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="31e27-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="31e27-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


