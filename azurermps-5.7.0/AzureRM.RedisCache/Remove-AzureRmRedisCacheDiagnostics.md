---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: fca64401f4671db63d76d491476f0e276e92055a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431639"
---
# <span data-ttu-id="c8648-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c8648-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="c8648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8648-102">SYNOPSIS</span></span>
<span data-ttu-id="c8648-103">Desabilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8648-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8648-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8648-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8648-105">DESCRIPTION</span></span>
<span data-ttu-id="c8648-106">O cmdlet **Remove-AzureRmRedisCacheDiagnostics** desabilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8648-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="c8648-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8648-107">EXAMPLES</span></span>

### <span data-ttu-id="c8648-108">Exemplo 1: desabilitar o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="c8648-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="c8648-109">Esse comando desabilita o diagnóstico no cache do Azure Redis especificado.</span><span class="sxs-lookup"><span data-stu-id="c8648-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="c8648-110">Isso desabilita o diagnóstico para todos os caches do Redis do Azure na mesma região da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c8648-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="c8648-111">OS</span><span class="sxs-lookup"><span data-stu-id="c8648-111">PARAMETERS</span></span>

### <span data-ttu-id="c8648-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8648-112">-DefaultProfile</span></span>
<span data-ttu-id="c8648-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8648-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8648-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8648-114">-Name</span></span>
<span data-ttu-id="c8648-115">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="c8648-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="c8648-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8648-116">-ResourceGroupName</span></span>
<span data-ttu-id="c8648-117">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="c8648-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="c8648-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8648-118">-Confirm</span></span>
<span data-ttu-id="c8648-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8648-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8648-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8648-120">-WhatIf</span></span>
<span data-ttu-id="c8648-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8648-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8648-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8648-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8648-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8648-123">CommonParameters</span></span>
<span data-ttu-id="c8648-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8648-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8648-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8648-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8648-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8648-126">INPUTS</span></span>

### <span data-ttu-id="c8648-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c8648-127">None</span></span>

## <span data-ttu-id="c8648-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8648-128">OUTPUTS</span></span>

### <span data-ttu-id="c8648-129">Sem</span><span class="sxs-lookup"><span data-stu-id="c8648-129">Void</span></span>

## <span data-ttu-id="c8648-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8648-130">NOTES</span></span>
* <span data-ttu-id="c8648-131">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="c8648-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c8648-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8648-132">RELATED LINKS</span></span>

[<span data-ttu-id="c8648-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c8648-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


