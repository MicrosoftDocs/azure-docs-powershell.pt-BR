---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889355"
---
# <span data-ttu-id="7cd8a-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="7cd8a-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="7cd8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd8a-103">Listar todos os Skus de recurso de computação</span><span class="sxs-lookup"><span data-stu-id="7cd8a-103">List all compute resource Skus</span></span>

## <span data-ttu-id="7cd8a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7cd8a-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd8a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7cd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd8a-106">Listar todos os Skus de recurso de computação</span><span class="sxs-lookup"><span data-stu-id="7cd8a-106">List all compute resource Skus</span></span>

## <span data-ttu-id="7cd8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd8a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7cd8a-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="7cd8a-109">Listar todos os skus de recurso de computação na região do Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="7cd8a-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="7cd8a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-110">PARAMETERS</span></span>

### <span data-ttu-id="7cd8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd8a-111">-DefaultProfile</span></span>
<span data-ttu-id="7cd8a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7cd8a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cd8a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7cd8a-113">-Location</span></span>
<span data-ttu-id="7cd8a-114">Especifica um local dos skus disponíveis para listar.</span><span class="sxs-lookup"><span data-stu-id="7cd8a-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd8a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd8a-115">CommonParameters</span></span>
<span data-ttu-id="7cd8a-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd8a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd8a-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cd8a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd8a-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-118">INPUTS</span></span>

### <span data-ttu-id="7cd8a-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd8a-119">System.String</span></span>

## <span data-ttu-id="7cd8a-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-120">OUTPUTS</span></span>

### <span data-ttu-id="7cd8a-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="7cd8a-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="7cd8a-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="7cd8a-122">NOTES</span></span>

## <span data-ttu-id="7cd8a-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cd8a-123">RELATED LINKS</span></span>
