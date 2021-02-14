---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115481"
---
# <span data-ttu-id="5b8b8-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="5b8b8-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="5b8b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8b8-103">Listar todas as SKIs de recursos de computação</span><span class="sxs-lookup"><span data-stu-id="5b8b8-103">List all compute resource Skus</span></span>

## <span data-ttu-id="5b8b8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b8b8-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b8b8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="5b8b8-106">Listar todas as SKIs de recursos de computação</span><span class="sxs-lookup"><span data-stu-id="5b8b8-106">List all compute resource Skus</span></span>

## <span data-ttu-id="5b8b8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b8b8-107">EXAMPLES</span></span>

### <span data-ttu-id="5b8b8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b8b8-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="5b8b8-109">Listar todas as SKIs de recursos de computação na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="5b8b8-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="5b8b8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b8b8-110">PARAMETERS</span></span>

### <span data-ttu-id="5b8b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b8b8-111">-DefaultProfile</span></span>
<span data-ttu-id="5b8b8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5b8b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b8b8-113">-Local</span><span class="sxs-lookup"><span data-stu-id="5b8b8-113">-Location</span></span>
<span data-ttu-id="5b8b8-114">Especifica um local das SKIs disponíveis para listar.</span><span class="sxs-lookup"><span data-stu-id="5b8b8-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="5b8b8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8b8-115">CommonParameters</span></span>
<span data-ttu-id="5b8b8-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b8b8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8b8-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b8b8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8b8-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b8b8-118">INPUTS</span></span>

### <span data-ttu-id="5b8b8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="5b8b8-119">System.String</span></span>

## <span data-ttu-id="5b8b8-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b8b8-120">OUTPUTS</span></span>

### <span data-ttu-id="5b8b8-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="5b8b8-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="5b8b8-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5b8b8-122">NOTES</span></span>

## <span data-ttu-id="5b8b8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b8b8-123">RELATED LINKS</span></span>
