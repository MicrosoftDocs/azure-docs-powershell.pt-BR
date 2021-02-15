---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118163"
---
# <span data-ttu-id="2cf4f-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2cf4f-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="2cf4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cf4f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf4f-103">Desabilita o diagnóstico em um Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="2cf4f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cf4f-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf4f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2cf4f-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf4f-106">O cmdlet **Remove-AzRedisCacheDiagnostic** desabilita o diagnóstico em um Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="2cf4f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2cf4f-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf4f-108">Exemplo 1: Desabilitar o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="2cf4f-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="2cf4f-109">Esse comando desabilita o diagnóstico no Cache de Redis do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="2cf4f-110">Isso desabilita o diagnóstico de todos os Caches do Azure Redis na mesma região da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="2cf4f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cf4f-111">PARAMETERS</span></span>

### <span data-ttu-id="2cf4f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf4f-112">-DefaultProfile</span></span>
<span data-ttu-id="2cf4f-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cf4f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cf4f-114">-Name</span></span>
<span data-ttu-id="2cf4f-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="2cf4f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf4f-116">-ResourceGroupName</span></span>
<span data-ttu-id="2cf4f-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="2cf4f-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2cf4f-118">-Confirm</span></span>
<span data-ttu-id="2cf4f-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf4f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf4f-120">-WhatIf</span></span>
<span data-ttu-id="2cf4f-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf4f-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf4f-123">CommonParameters</span></span>
<span data-ttu-id="2cf4f-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf4f-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf4f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf4f-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="2cf4f-126">INPUTS</span></span>

### <span data-ttu-id="2cf4f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2cf4f-127">System.String</span></span>

## <span data-ttu-id="2cf4f-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="2cf4f-128">OUTPUTS</span></span>

### <span data-ttu-id="2cf4f-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="2cf4f-129">System.Void</span></span>

## <span data-ttu-id="2cf4f-130">Notas</span><span class="sxs-lookup"><span data-stu-id="2cf4f-130">NOTES</span></span>
* <span data-ttu-id="2cf4f-131">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="2cf4f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2cf4f-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cf4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="2cf4f-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2cf4f-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


