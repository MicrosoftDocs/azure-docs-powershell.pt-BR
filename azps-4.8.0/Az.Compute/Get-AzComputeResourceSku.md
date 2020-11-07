---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948154"
---
# <span data-ttu-id="e1bcb-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="e1bcb-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="e1bcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bcb-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="e1bcb-103">List all compute resource Skus</span></span>

## <span data-ttu-id="e1bcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1bcb-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bcb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1bcb-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bcb-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="e1bcb-106">List all compute resource Skus</span></span>

## <span data-ttu-id="e1bcb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1bcb-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bcb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1bcb-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="e1bcb-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="e1bcb-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="e1bcb-110">OS</span><span class="sxs-lookup"><span data-stu-id="e1bcb-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bcb-111">-DefaultProfile</span></span>
<span data-ttu-id="e1bcb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1bcb-113">-Local</span><span class="sxs-lookup"><span data-stu-id="e1bcb-113">-Location</span></span>
<span data-ttu-id="e1bcb-114">Especifica um local da lista de SKUs disponíveis a serem listados.</span><span class="sxs-lookup"><span data-stu-id="e1bcb-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="e1bcb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bcb-115">CommonParameters</span></span>
<span data-ttu-id="e1bcb-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bcb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bcb-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1bcb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bcb-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1bcb-118">INPUTS</span></span>

### <span data-ttu-id="e1bcb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e1bcb-119">System.String</span></span>

## <span data-ttu-id="e1bcb-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1bcb-120">OUTPUTS</span></span>

### <span data-ttu-id="e1bcb-121">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="e1bcb-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="e1bcb-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1bcb-122">NOTES</span></span>

## <span data-ttu-id="e1bcb-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1bcb-123">RELATED LINKS</span></span>
