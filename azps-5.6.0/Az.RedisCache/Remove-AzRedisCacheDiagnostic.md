---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: d32fe3286a8c6e4b723137f8b20921c79caa45be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889618"
---
# <span data-ttu-id="e4977-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e4977-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="e4977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4977-102">SYNOPSIS</span></span>
<span data-ttu-id="e4977-103">Desabilita os diagnósticos em um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e4977-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e4977-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4977-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4977-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4977-105">DESCRIPTION</span></span>
<span data-ttu-id="e4977-106">O cmdlet **Remove-AzRedisCacheDiagnostic** desabilita os diagnósticos em um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e4977-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e4977-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4977-107">EXAMPLES</span></span>

### <span data-ttu-id="e4977-108">Exemplo 1: Desabilitar diagnósticos</span><span class="sxs-lookup"><span data-stu-id="e4977-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="e4977-109">Este comando desabilita os diagnósticos no Cache do Azure Redis especificado.</span><span class="sxs-lookup"><span data-stu-id="e4977-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="e4977-110">Isso desabilita o diagnóstico de todos os Caches do Azure Redis na mesma região da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e4977-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="e4977-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4977-111">PARAMETERS</span></span>

### <span data-ttu-id="e4977-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4977-112">-DefaultProfile</span></span>
<span data-ttu-id="e4977-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4977-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4977-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e4977-114">-Name</span></span>
<span data-ttu-id="e4977-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e4977-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="e4977-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4977-116">-ResourceGroupName</span></span>
<span data-ttu-id="e4977-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="e4977-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e4977-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4977-118">-Confirm</span></span>
<span data-ttu-id="e4977-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4977-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4977-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4977-120">-WhatIf</span></span>
<span data-ttu-id="e4977-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4977-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4977-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4977-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4977-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4977-123">CommonParameters</span></span>
<span data-ttu-id="e4977-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4977-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4977-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4977-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4977-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4977-126">INPUTS</span></span>

### <span data-ttu-id="e4977-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e4977-127">System.String</span></span>

## <span data-ttu-id="e4977-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4977-128">OUTPUTS</span></span>

### <span data-ttu-id="e4977-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4977-129">System.Void</span></span>

## <span data-ttu-id="e4977-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4977-130">NOTES</span></span>
* <span data-ttu-id="e4977-131">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="e4977-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e4977-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4977-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4977-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e4977-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


