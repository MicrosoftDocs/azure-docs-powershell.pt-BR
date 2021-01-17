---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426843"
---
# <span data-ttu-id="e3236-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e3236-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="e3236-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3236-102">SYNOPSIS</span></span>
<span data-ttu-id="e3236-103">Obtém um (s) cache (es).</span><span class="sxs-lookup"><span data-stu-id="e3236-103">Gets a cache(s).</span></span>

## <span data-ttu-id="e3236-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3236-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3236-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3236-105">DESCRIPTION</span></span>
<span data-ttu-id="e3236-106">O cmdlet **Get-AzHpcCache** Obtém um único cache, cache (s) em um grupo de recursos específico ou uma lista de uma grande largura da assinatura de caches.</span><span class="sxs-lookup"><span data-stu-id="e3236-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="e3236-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3236-107">EXAMPLES</span></span>

### <span data-ttu-id="e3236-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3236-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="e3236-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3236-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="e3236-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e3236-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="e3236-111">OS</span><span class="sxs-lookup"><span data-stu-id="e3236-111">PARAMETERS</span></span>

### <span data-ttu-id="e3236-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3236-112">-DefaultProfile</span></span>
<span data-ttu-id="e3236-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3236-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3236-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3236-114">-Name</span></span>
<span data-ttu-id="e3236-115">Nome do cache específico.</span><span class="sxs-lookup"><span data-stu-id="e3236-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="e3236-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3236-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3236-117">Nome do grupo de recursos sob o qual você deseja listar cache (s).</span><span class="sxs-lookup"><span data-stu-id="e3236-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="e3236-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3236-118">CommonParameters</span></span>
<span data-ttu-id="e3236-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3236-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3236-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3236-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3236-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3236-121">INPUTS</span></span>

### <span data-ttu-id="e3236-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e3236-122">System.String</span></span>

## <span data-ttu-id="e3236-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3236-123">OUTPUTS</span></span>

### <span data-ttu-id="e3236-124">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="e3236-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="e3236-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3236-125">NOTES</span></span>

## <span data-ttu-id="e3236-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3236-126">RELATED LINKS</span></span>
