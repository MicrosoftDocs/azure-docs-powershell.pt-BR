---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428573"
---
# <span data-ttu-id="8890d-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="8890d-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="8890d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8890d-102">SYNOPSIS</span></span>
<span data-ttu-id="8890d-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="8890d-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8890d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8890d-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8890d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8890d-105">DESCRIPTION</span></span>
<span data-ttu-id="8890d-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="8890d-106">List all compute resource Skus</span></span>

## <span data-ttu-id="8890d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8890d-107">EXAMPLES</span></span>

### <span data-ttu-id="8890d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8890d-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="8890d-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="8890d-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="8890d-110">OS</span><span class="sxs-lookup"><span data-stu-id="8890d-110">PARAMETERS</span></span>

### <span data-ttu-id="8890d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8890d-111">-DefaultProfile</span></span>
<span data-ttu-id="8890d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8890d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8890d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8890d-113">CommonParameters</span></span>
<span data-ttu-id="8890d-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8890d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8890d-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8890d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8890d-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8890d-116">INPUTS</span></span>

### <span data-ttu-id="8890d-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8890d-117">None</span></span>

## <span data-ttu-id="8890d-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8890d-118">OUTPUTS</span></span>

### <span data-ttu-id="8890d-119">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="8890d-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="8890d-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8890d-120">NOTES</span></span>

## <span data-ttu-id="8890d-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8890d-121">RELATED LINKS</span></span>