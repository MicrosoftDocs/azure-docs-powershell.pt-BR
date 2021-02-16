---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113175"
---
# <span data-ttu-id="20386-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="20386-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="20386-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20386-102">SYNOPSIS</span></span>
<span data-ttu-id="20386-103">Obtém um(s) cache(s).</span><span class="sxs-lookup"><span data-stu-id="20386-103">Gets a cache(s).</span></span>

## <span data-ttu-id="20386-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20386-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20386-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20386-105">DESCRIPTION</span></span>
<span data-ttu-id="20386-106">O cmdlet **Get-AzHpcCache** obtém um único cache, cache(s) em um grupo de recursos específico ou lista de caches de toda a assinatura.</span><span class="sxs-lookup"><span data-stu-id="20386-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="20386-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20386-107">EXAMPLES</span></span>

### <span data-ttu-id="20386-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20386-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="20386-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="20386-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="20386-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="20386-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="20386-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20386-111">PARAMETERS</span></span>

### <span data-ttu-id="20386-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20386-112">-DefaultProfile</span></span>
<span data-ttu-id="20386-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20386-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20386-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="20386-114">-Name</span></span>
<span data-ttu-id="20386-115">Nome de cache específico.</span><span class="sxs-lookup"><span data-stu-id="20386-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="20386-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20386-116">-ResourceGroupName</span></span>
<span data-ttu-id="20386-117">Nome do grupo de recursos no qual você deseja listar caches.</span><span class="sxs-lookup"><span data-stu-id="20386-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="20386-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20386-118">CommonParameters</span></span>
<span data-ttu-id="20386-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20386-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20386-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20386-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20386-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="20386-121">INPUTS</span></span>

### <span data-ttu-id="20386-122">System.String</span><span class="sxs-lookup"><span data-stu-id="20386-122">System.String</span></span>

## <span data-ttu-id="20386-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="20386-123">OUTPUTS</span></span>

### <span data-ttu-id="20386-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="20386-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="20386-125">Notas</span><span class="sxs-lookup"><span data-stu-id="20386-125">NOTES</span></span>

## <span data-ttu-id="20386-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20386-126">RELATED LINKS</span></span>
