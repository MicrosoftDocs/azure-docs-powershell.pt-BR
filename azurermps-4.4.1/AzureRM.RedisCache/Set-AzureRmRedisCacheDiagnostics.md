---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440564"
---
# <span data-ttu-id="bd4ca-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bd4ca-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="bd4ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4ca-103">Habilita o diagnóstico em um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd4ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd4ca-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd4ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd4ca-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4ca-106">O cmdlet **set-AzureRmRedisCacheDiagnostics** habilita o diagnóstico para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="bd4ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd4ca-107">EXAMPLES</span></span>

### <span data-ttu-id="bd4ca-108">Exemplo 1: habilitar o diagnóstico</span><span class="sxs-lookup"><span data-stu-id="bd4ca-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="bd4ca-109">Esse comando habilita o diagnóstico para um cache do Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="bd4ca-110">Esse comando habilitará o diagnóstico ou atualizará a conta de armazenamento de todos os caches do Redis do Azure na mesma região para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="bd4ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="bd4ca-111">PARAMETERS</span></span>

### <span data-ttu-id="bd4ca-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd4ca-112">-Name</span></span>
<span data-ttu-id="bd4ca-113">Especifica o nome do cache.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="bd4ca-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4ca-114">-ResourceGroupName</span></span>
<span data-ttu-id="bd4ca-115">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="bd4ca-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bd4ca-116">-StorageAccountId</span></span>
<span data-ttu-id="bd4ca-117">Especifica a ID do recurso da conta de armazenamento usada para armazenar os dados de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="bd4ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4ca-118">-DefaultProfile</span></span>
<span data-ttu-id="bd4ca-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd4ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4ca-120">CommonParameters</span></span>
<span data-ttu-id="bd4ca-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd4ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4ca-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4ca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4ca-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd4ca-123">INPUTS</span></span>

### <span data-ttu-id="bd4ca-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bd4ca-124">None</span></span>

## <span data-ttu-id="bd4ca-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd4ca-125">OUTPUTS</span></span>

### <span data-ttu-id="bd4ca-126">Sem</span><span class="sxs-lookup"><span data-stu-id="bd4ca-126">Void</span></span>

## <span data-ttu-id="bd4ca-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd4ca-127">NOTES</span></span>
* <span data-ttu-id="bd4ca-128">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="bd4ca-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bd4ca-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd4ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="bd4ca-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="bd4ca-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


