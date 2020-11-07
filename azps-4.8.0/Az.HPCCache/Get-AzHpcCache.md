---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954998"
---
# <span data-ttu-id="08163-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="08163-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="08163-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08163-102">SYNOPSIS</span></span>
<span data-ttu-id="08163-103">Obtém um (s) cache (es).</span><span class="sxs-lookup"><span data-stu-id="08163-103">Gets a cache(s).</span></span>

## <span data-ttu-id="08163-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08163-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08163-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08163-105">DESCRIPTION</span></span>
<span data-ttu-id="08163-106">O cmdlet **Get-AzHpcCache** Obtém um único cache, cache (s) em um grupo de recursos específico ou uma lista de uma grande largura da assinatura de caches.</span><span class="sxs-lookup"><span data-stu-id="08163-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="08163-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08163-107">EXAMPLES</span></span>

### <span data-ttu-id="08163-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="08163-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="08163-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="08163-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="08163-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="08163-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="08163-111">OS</span><span class="sxs-lookup"><span data-stu-id="08163-111">PARAMETERS</span></span>

### <span data-ttu-id="08163-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08163-112">-DefaultProfile</span></span>
<span data-ttu-id="08163-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08163-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08163-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="08163-114">-Name</span></span>
<span data-ttu-id="08163-115">Nome do cache específico.</span><span class="sxs-lookup"><span data-stu-id="08163-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="08163-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08163-116">-ResourceGroupName</span></span>
<span data-ttu-id="08163-117">Nome do grupo de recursos sob o qual você deseja listar cache (s).</span><span class="sxs-lookup"><span data-stu-id="08163-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="08163-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08163-118">CommonParameters</span></span>
<span data-ttu-id="08163-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08163-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08163-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08163-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08163-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08163-121">INPUTS</span></span>

### <span data-ttu-id="08163-122">System. String</span><span class="sxs-lookup"><span data-stu-id="08163-122">System.String</span></span>

## <span data-ttu-id="08163-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08163-123">OUTPUTS</span></span>

### <span data-ttu-id="08163-124">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="08163-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="08163-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08163-125">NOTES</span></span>

## <span data-ttu-id="08163-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08163-126">RELATED LINKS</span></span>
