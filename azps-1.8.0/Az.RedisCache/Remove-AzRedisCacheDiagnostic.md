---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 6fcb8c2079ad26cc98c151aa55af00e475568db5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599538"
---
# <span data-ttu-id="e5a9d-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e5a9d-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="e5a9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a9d-103">Desabilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e5a9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5a9d-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a9d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a9d-106">O cmdlet **Remove-AzRedisCacheDiagnostic** desabilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e5a9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5a9d-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a9d-108">Exemplo 1: desabilitar o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e5a9d-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="e5a9d-109">Esse comando desabilita o diagnóstico no cache do Azure Redis especificado.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="e5a9d-110">Isso desabilita o diagnóstico para todos os caches do Redis do Azure na mesma região da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="e5a9d-111">OS</span><span class="sxs-lookup"><span data-stu-id="e5a9d-111">PARAMETERS</span></span>

### <span data-ttu-id="e5a9d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a9d-112">-DefaultProfile</span></span>
<span data-ttu-id="e5a9d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a9d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5a9d-114">-Name</span></span>
<span data-ttu-id="e5a9d-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="e5a9d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a9d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e5a9d-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e5a9d-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e5a9d-118">-Confirm</span></span>
<span data-ttu-id="e5a9d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a9d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a9d-120">-WhatIf</span></span>
<span data-ttu-id="e5a9d-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a9d-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a9d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a9d-123">CommonParameters</span></span>
<span data-ttu-id="e5a9d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a9d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a9d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a9d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a9d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5a9d-126">INPUTS</span></span>

### <span data-ttu-id="e5a9d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a9d-127">System.String</span></span>

## <span data-ttu-id="e5a9d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5a9d-128">OUTPUTS</span></span>

### <span data-ttu-id="e5a9d-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e5a9d-129">System.Void</span></span>

## <span data-ttu-id="e5a9d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5a9d-130">NOTES</span></span>
* <span data-ttu-id="e5a9d-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="e5a9d-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e5a9d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5a9d-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5a9d-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e5a9d-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


