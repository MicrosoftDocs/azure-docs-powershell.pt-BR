---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893164"
---
# <span data-ttu-id="3c67a-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="3c67a-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="3c67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c67a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c67a-103">Obtém um(s) cache(s).</span><span class="sxs-lookup"><span data-stu-id="3c67a-103">Gets a cache(s).</span></span>

## <span data-ttu-id="3c67a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c67a-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c67a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c67a-105">DESCRIPTION</span></span>
<span data-ttu-id="3c67a-106">O cmdlet **Get-AzHpcCache** obtém um único cache, cache(s) em um grupo de recursos específico ou uma lista ampla de assinaturas de caches.</span><span class="sxs-lookup"><span data-stu-id="3c67a-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="3c67a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c67a-107">EXAMPLES</span></span>

### <span data-ttu-id="3c67a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c67a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="3c67a-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c67a-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="3c67a-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3c67a-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="3c67a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c67a-111">PARAMETERS</span></span>

### <span data-ttu-id="3c67a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c67a-112">-DefaultProfile</span></span>
<span data-ttu-id="3c67a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c67a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c67a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3c67a-114">-Name</span></span>
<span data-ttu-id="3c67a-115">Nome do cache específico.</span><span class="sxs-lookup"><span data-stu-id="3c67a-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c67a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c67a-116">-ResourceGroupName</span></span>
<span data-ttu-id="3c67a-117">Nome do grupo de recursos no qual você deseja listar caches.</span><span class="sxs-lookup"><span data-stu-id="3c67a-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="3c67a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c67a-118">CommonParameters</span></span>
<span data-ttu-id="3c67a-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c67a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c67a-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c67a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c67a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c67a-121">INPUTS</span></span>

### <span data-ttu-id="3c67a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3c67a-122">System.String</span></span>

## <span data-ttu-id="3c67a-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c67a-123">OUTPUTS</span></span>

### <span data-ttu-id="3c67a-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="3c67a-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="3c67a-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c67a-125">NOTES</span></span>

## <span data-ttu-id="3c67a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c67a-126">RELATED LINKS</span></span>
