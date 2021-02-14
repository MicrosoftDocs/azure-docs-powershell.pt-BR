---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117211"
---
# <span data-ttu-id="d972f-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d972f-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d972f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d972f-102">SYNOPSIS</span></span>
<span data-ttu-id="d972f-103">Remove o cronograma de patch.</span><span class="sxs-lookup"><span data-stu-id="d972f-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="d972f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d972f-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d972f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d972f-105">DESCRIPTION</span></span>
<span data-ttu-id="d972f-106">O cmdlet **Remove-AzRedisCachePatchSchedule** remove o cronograma de patch de um cache no Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d972f-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d972f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d972f-107">EXAMPLES</span></span>

### <span data-ttu-id="d972f-108">Exemplo 1: Remover o cronograma de patch</span><span class="sxs-lookup"><span data-stu-id="d972f-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="d972f-109">Esse comando remove o cronograma de patch do cache chamado RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="d972f-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="d972f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d972f-110">PARAMETERS</span></span>

### <span data-ttu-id="d972f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d972f-111">-DefaultProfile</span></span>
<span data-ttu-id="d972f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d972f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d972f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d972f-113">-Name</span></span>
<span data-ttu-id="d972f-114">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="d972f-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="d972f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d972f-115">-PassThru</span></span>
<span data-ttu-id="d972f-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d972f-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d972f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d972f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d972f-118">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="d972f-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d972f-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d972f-119">-Confirm</span></span>
<span data-ttu-id="d972f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d972f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d972f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d972f-121">-WhatIf</span></span>
<span data-ttu-id="d972f-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d972f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d972f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d972f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d972f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d972f-124">CommonParameters</span></span>
<span data-ttu-id="d972f-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d972f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d972f-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d972f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d972f-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="d972f-127">INPUTS</span></span>

### <span data-ttu-id="d972f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d972f-128">System.String</span></span>

## <span data-ttu-id="d972f-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="d972f-129">OUTPUTS</span></span>

### <span data-ttu-id="d972f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d972f-130">System.Boolean</span></span>

## <span data-ttu-id="d972f-131">Notas</span><span class="sxs-lookup"><span data-stu-id="d972f-131">NOTES</span></span>
* <span data-ttu-id="d972f-132">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="d972f-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d972f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d972f-133">RELATED LINKS</span></span>

[<span data-ttu-id="d972f-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d972f-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="d972f-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d972f-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="d972f-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d972f-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


