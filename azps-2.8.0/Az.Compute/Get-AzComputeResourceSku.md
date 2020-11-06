---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597482"
---
# <span data-ttu-id="55dba-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="55dba-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="55dba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55dba-102">SYNOPSIS</span></span>
<span data-ttu-id="55dba-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="55dba-103">List all compute resource Skus</span></span>

## <span data-ttu-id="55dba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55dba-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55dba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55dba-105">DESCRIPTION</span></span>
<span data-ttu-id="55dba-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="55dba-106">List all compute resource Skus</span></span>

## <span data-ttu-id="55dba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55dba-107">EXAMPLES</span></span>

### <span data-ttu-id="55dba-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55dba-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="55dba-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="55dba-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="55dba-110">OS</span><span class="sxs-lookup"><span data-stu-id="55dba-110">PARAMETERS</span></span>

### <span data-ttu-id="55dba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dba-111">-DefaultProfile</span></span>
<span data-ttu-id="55dba-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55dba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55dba-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dba-113">CommonParameters</span></span>
<span data-ttu-id="55dba-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55dba-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dba-115">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55dba-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dba-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55dba-116">INPUTS</span></span>

### <span data-ttu-id="55dba-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="55dba-117">None</span></span>

## <span data-ttu-id="55dba-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55dba-118">OUTPUTS</span></span>

### <span data-ttu-id="55dba-119">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="55dba-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="55dba-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55dba-120">NOTES</span></span>

## <span data-ttu-id="55dba-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55dba-121">RELATED LINKS</span></span>
