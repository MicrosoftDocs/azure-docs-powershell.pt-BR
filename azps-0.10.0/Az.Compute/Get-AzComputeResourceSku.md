---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777057"
---
# <span data-ttu-id="f6530-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="f6530-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="f6530-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6530-102">SYNOPSIS</span></span>
<span data-ttu-id="f6530-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="f6530-103">List all compute resource Skus</span></span>

## <span data-ttu-id="f6530-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6530-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6530-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6530-105">DESCRIPTION</span></span>
<span data-ttu-id="f6530-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="f6530-106">List all compute resource Skus</span></span>

## <span data-ttu-id="f6530-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6530-107">EXAMPLES</span></span>

### <span data-ttu-id="f6530-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6530-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="f6530-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f6530-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="f6530-110">OS</span><span class="sxs-lookup"><span data-stu-id="f6530-110">PARAMETERS</span></span>

### <span data-ttu-id="f6530-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6530-111">-DefaultProfile</span></span>
<span data-ttu-id="f6530-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6530-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6530-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6530-113">CommonParameters</span></span>
<span data-ttu-id="f6530-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6530-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6530-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6530-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6530-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6530-116">INPUTS</span></span>

### <span data-ttu-id="f6530-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6530-117">None</span></span>

## <span data-ttu-id="f6530-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6530-118">OUTPUTS</span></span>

### <span data-ttu-id="f6530-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="f6530-119">System.Object</span></span>

## <span data-ttu-id="f6530-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6530-120">NOTES</span></span>

## <span data-ttu-id="f6530-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6530-121">RELATED LINKS</span></span>

