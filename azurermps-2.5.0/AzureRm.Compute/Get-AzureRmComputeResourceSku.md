---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786576"
---
# <span data-ttu-id="547b0-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="547b0-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="547b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="547b0-102">SYNOPSIS</span></span>
<span data-ttu-id="547b0-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="547b0-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="547b0-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="547b0-105">DESCRIPTION</span></span>
<span data-ttu-id="547b0-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="547b0-106">List all compute resource Skus</span></span>

## <span data-ttu-id="547b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="547b0-107">EXAMPLES</span></span>

### <span data-ttu-id="547b0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="547b0-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="547b0-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="547b0-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="547b0-110">OS</span><span class="sxs-lookup"><span data-stu-id="547b0-110">PARAMETERS</span></span>

### <span data-ttu-id="547b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547b0-111">-DefaultProfile</span></span>
<span data-ttu-id="547b0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="547b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547b0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547b0-113">CommonParameters</span></span>
<span data-ttu-id="547b0-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547b0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547b0-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="547b0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547b0-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="547b0-116">INPUTS</span></span>

### <span data-ttu-id="547b0-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="547b0-117">None</span></span>

## <span data-ttu-id="547b0-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="547b0-118">OUTPUTS</span></span>

### <span data-ttu-id="547b0-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="547b0-119">System.Object</span></span>

## <span data-ttu-id="547b0-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="547b0-120">NOTES</span></span>

## <span data-ttu-id="547b0-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="547b0-121">RELATED LINKS</span></span>

