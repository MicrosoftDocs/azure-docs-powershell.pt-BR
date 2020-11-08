---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111457"
---
# <span data-ttu-id="9462a-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9462a-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="9462a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9462a-102">SYNOPSIS</span></span>
<span data-ttu-id="9462a-103">Habilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="9462a-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="9462a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9462a-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9462a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9462a-105">DESCRIPTION</span></span>
<span data-ttu-id="9462a-106">O cmdlet **set-AzRedisCacheDiagnostic** habilita o diagnóstico para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="9462a-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="9462a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9462a-107">EXAMPLES</span></span>

### <span data-ttu-id="9462a-108">Exemplo 1: habilitar o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="9462a-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="9462a-109">Esse comando habilita o diagnóstico para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="9462a-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="9462a-110">Esse comando habilitará o diagnóstico ou atualizará a conta de armazenamento de todos os caches do Redis do Azure na mesma região para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="9462a-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="9462a-111">OS</span><span class="sxs-lookup"><span data-stu-id="9462a-111">PARAMETERS</span></span>

### <span data-ttu-id="9462a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9462a-112">-DefaultProfile</span></span>
<span data-ttu-id="9462a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9462a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9462a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9462a-114">-Name</span></span>
<span data-ttu-id="9462a-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="9462a-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="9462a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9462a-116">-ResourceGroupName</span></span>
<span data-ttu-id="9462a-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="9462a-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="9462a-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9462a-118">-StorageAccountId</span></span>
<span data-ttu-id="9462a-119">Especifica a ID do recurso da conta de armazenamento usada para armazenar os dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9462a-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="9462a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9462a-120">-Confirm</span></span>
<span data-ttu-id="9462a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9462a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9462a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9462a-122">-WhatIf</span></span>
<span data-ttu-id="9462a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9462a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9462a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9462a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9462a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9462a-125">CommonParameters</span></span>
<span data-ttu-id="9462a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9462a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9462a-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9462a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9462a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9462a-128">INPUTS</span></span>

### <span data-ttu-id="9462a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9462a-129">System.String</span></span>

## <span data-ttu-id="9462a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9462a-130">OUTPUTS</span></span>

### <span data-ttu-id="9462a-131">System. void</span><span class="sxs-lookup"><span data-stu-id="9462a-131">System.Void</span></span>

## <span data-ttu-id="9462a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9462a-132">NOTES</span></span>
* <span data-ttu-id="9462a-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="9462a-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9462a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9462a-134">RELATED LINKS</span></span>

[<span data-ttu-id="9462a-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9462a-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


