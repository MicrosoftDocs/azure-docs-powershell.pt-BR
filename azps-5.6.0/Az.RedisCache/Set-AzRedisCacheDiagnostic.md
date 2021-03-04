---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: ee6e2848325222d86271bfd70705ec7aa855cbb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891763"
---
# <span data-ttu-id="d7b44-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d7b44-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="d7b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7b44-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b44-103">Habilita diagnósticos em um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d7b44-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="d7b44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d7b44-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b44-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d7b44-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b44-106">O cmdlet **Set-AzRedisCacheDiagnostic** habilita diagnósticos para um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d7b44-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="d7b44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7b44-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b44-108">Exemplo 1: Habilitar diagnósticos</span><span class="sxs-lookup"><span data-stu-id="d7b44-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="d7b44-109">Este comando habilita diagnósticos para um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d7b44-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="d7b44-110">Este comando habilita o diagnóstico ou atualiza a conta de armazenamento de todos os Caches do Azure Redis na mesma região da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d7b44-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="d7b44-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d7b44-111">PARAMETERS</span></span>

### <span data-ttu-id="d7b44-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b44-112">-DefaultProfile</span></span>
<span data-ttu-id="d7b44-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d7b44-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7b44-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b44-114">-Name</span></span>
<span data-ttu-id="d7b44-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="d7b44-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d7b44-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b44-116">-ResourceGroupName</span></span>
<span data-ttu-id="d7b44-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="d7b44-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="d7b44-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d7b44-118">-StorageAccountId</span></span>
<span data-ttu-id="d7b44-119">Especifica a ID de recurso da conta de armazenamento usada para armazenar os dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d7b44-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="d7b44-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7b44-120">-Confirm</span></span>
<span data-ttu-id="d7b44-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b44-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b44-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b44-122">-WhatIf</span></span>
<span data-ttu-id="d7b44-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7b44-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7b44-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7b44-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b44-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b44-125">CommonParameters</span></span>
<span data-ttu-id="d7b44-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b44-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b44-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b44-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b44-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7b44-128">INPUTS</span></span>

### <span data-ttu-id="d7b44-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d7b44-129">System.String</span></span>

## <span data-ttu-id="d7b44-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d7b44-130">OUTPUTS</span></span>

### <span data-ttu-id="d7b44-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="d7b44-131">System.Void</span></span>

## <span data-ttu-id="d7b44-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="d7b44-132">NOTES</span></span>
* <span data-ttu-id="d7b44-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="d7b44-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d7b44-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7b44-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7b44-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d7b44-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


