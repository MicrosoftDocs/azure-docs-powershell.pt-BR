---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955779"
---
# <span data-ttu-id="81227-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="81227-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="81227-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81227-102">SYNOPSIS</span></span>
<span data-ttu-id="81227-103">Obtém as cotas de serviço em lotes para a sua assinatura em determinado local.</span><span class="sxs-lookup"><span data-stu-id="81227-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="81227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81227-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81227-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81227-105">DESCRIPTION</span></span>
<span data-ttu-id="81227-106">Obtém as cotas de serviço em lotes para a assinatura especificada em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="81227-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="81227-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81227-107">EXAMPLES</span></span>

### <span data-ttu-id="81227-108">Exemplo 1: obter as cotas de serviço em lotes para a assinatura na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="81227-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="81227-109">Este comando obtém as cotas para a assinatura atual na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="81227-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="81227-110">O valor de retorno indica que essa assinatura pode criar apenas uma conta em lotes nessa região.</span><span class="sxs-lookup"><span data-stu-id="81227-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="81227-111">OS</span><span class="sxs-lookup"><span data-stu-id="81227-111">PARAMETERS</span></span>

### <span data-ttu-id="81227-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81227-112">-DefaultProfile</span></span>
<span data-ttu-id="81227-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81227-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81227-114">-Local</span><span class="sxs-lookup"><span data-stu-id="81227-114">-Location</span></span>
<span data-ttu-id="81227-115">Especifica a região para a qual esse cmdlet verifica as cotas.</span><span class="sxs-lookup"><span data-stu-id="81227-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="81227-116">Para obter mais informações, consulte regiões do Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="81227-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81227-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81227-117">CommonParameters</span></span>
<span data-ttu-id="81227-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81227-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81227-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81227-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81227-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81227-120">INPUTS</span></span>

### <span data-ttu-id="81227-121">System. String</span><span class="sxs-lookup"><span data-stu-id="81227-121">System.String</span></span>

## <span data-ttu-id="81227-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81227-122">OUTPUTS</span></span>

### <span data-ttu-id="81227-123">Microsoft.Azure.Commands.Batch. Modelos. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="81227-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="81227-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81227-124">NOTES</span></span>

## <span data-ttu-id="81227-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81227-125">RELATED LINKS</span></span>
