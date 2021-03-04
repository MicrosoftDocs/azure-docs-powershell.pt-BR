---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886262"
---
# <span data-ttu-id="f76cb-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="f76cb-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="f76cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f76cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f76cb-103">Obtém as cotas de serviço em lotes para sua assinatura no local determinado.</span><span class="sxs-lookup"><span data-stu-id="f76cb-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="f76cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f76cb-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f76cb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f76cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f76cb-106">Obtém as cotas de serviço em lotes para a assinatura especificada no local determinado.</span><span class="sxs-lookup"><span data-stu-id="f76cb-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="f76cb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f76cb-107">EXAMPLES</span></span>

### <span data-ttu-id="f76cb-108">Exemplo 1: Obter as cotas de serviço em lotes para a assinatura na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f76cb-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="f76cb-109">Este comando obtém as cotas da assinatura atual na região dos EUA Ocidental.</span><span class="sxs-lookup"><span data-stu-id="f76cb-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="f76cb-110">O valor de retorno indica que essa assinatura pode criar apenas uma conta Batch nessa região.</span><span class="sxs-lookup"><span data-stu-id="f76cb-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="f76cb-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f76cb-111">PARAMETERS</span></span>

### <span data-ttu-id="f76cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76cb-112">-DefaultProfile</span></span>
<span data-ttu-id="f76cb-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f76cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f76cb-114">-Location</span><span class="sxs-lookup"><span data-stu-id="f76cb-114">-Location</span></span>
<span data-ttu-id="f76cb-115">Especifica a região para a qual esse cmdlet verifica as cotas.</span><span class="sxs-lookup"><span data-stu-id="f76cb-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="f76cb-116">Para obter mais informações, consulte Regiões do Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="f76cb-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="f76cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76cb-117">CommonParameters</span></span>
<span data-ttu-id="f76cb-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f76cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76cb-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f76cb-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76cb-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f76cb-120">INPUTS</span></span>

### <span data-ttu-id="f76cb-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f76cb-121">System.String</span></span>

## <span data-ttu-id="f76cb-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f76cb-122">OUTPUTS</span></span>

### <span data-ttu-id="f76cb-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="f76cb-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="f76cb-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f76cb-124">NOTES</span></span>

## <span data-ttu-id="f76cb-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f76cb-125">RELATED LINKS</span></span>
