---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427637"
---
# <span data-ttu-id="7056f-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="7056f-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="7056f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7056f-102">SYNOPSIS</span></span>
<span data-ttu-id="7056f-103">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="7056f-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7056f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7056f-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="7056f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7056f-105">DESCRIPTION</span></span>
<span data-ttu-id="7056f-106">Listar todas as SKUs do recurso de computação</span><span class="sxs-lookup"><span data-stu-id="7056f-106">List all compute resource Skus</span></span>

## <span data-ttu-id="7056f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7056f-107">EXAMPLES</span></span>

### <span data-ttu-id="7056f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7056f-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="7056f-109">Listar todas as SKUs do recurso de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="7056f-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="7056f-110">OS</span><span class="sxs-lookup"><span data-stu-id="7056f-110">PARAMETERS</span></span>

### <span data-ttu-id="7056f-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7056f-111">CommonParameters</span></span>
<span data-ttu-id="7056f-112">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7056f-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7056f-113">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7056f-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7056f-114">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7056f-114">INPUTS</span></span>

### <span data-ttu-id="7056f-115">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7056f-115">None</span></span>


## <span data-ttu-id="7056f-116">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7056f-116">OUTPUTS</span></span>

### <span data-ttu-id="7056f-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="7056f-117">System.Object</span></span>

## <span data-ttu-id="7056f-118">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7056f-118">NOTES</span></span>

## <span data-ttu-id="7056f-119">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7056f-119">RELATED LINKS</span></span>

