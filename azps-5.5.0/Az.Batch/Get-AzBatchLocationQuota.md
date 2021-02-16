---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117955"
---
# <span data-ttu-id="7772f-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="7772f-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="7772f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7772f-102">SYNOPSIS</span></span>
<span data-ttu-id="7772f-103">Obtém as cotas de serviço em lotes da sua assinatura no local determinado.</span><span class="sxs-lookup"><span data-stu-id="7772f-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="7772f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7772f-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7772f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7772f-105">DESCRIPTION</span></span>
<span data-ttu-id="7772f-106">Obtém as cotas de serviço em lote para a assinatura especificada no local determinado.</span><span class="sxs-lookup"><span data-stu-id="7772f-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="7772f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7772f-107">EXAMPLES</span></span>

### <span data-ttu-id="7772f-108">Exemplo 1: Obter as cotas de serviço em lote para a assinatura na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="7772f-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="7772f-109">Esse comando obtém as cotas da assinatura atual na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="7772f-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="7772f-110">O valor de retorno indica que essa assinatura pode criar apenas uma conta em lotes nessa região.</span><span class="sxs-lookup"><span data-stu-id="7772f-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="7772f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7772f-111">PARAMETERS</span></span>

### <span data-ttu-id="7772f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7772f-112">-DefaultProfile</span></span>
<span data-ttu-id="7772f-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7772f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7772f-114">-Local</span><span class="sxs-lookup"><span data-stu-id="7772f-114">-Location</span></span>
<span data-ttu-id="7772f-115">Especifica a região para a qual este cmdlet verifica as cotas.</span><span class="sxs-lookup"><span data-stu-id="7772f-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="7772f-116">Para obter mais informações, consulte Regiões do Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="7772f-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="7772f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7772f-117">CommonParameters</span></span>
<span data-ttu-id="7772f-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7772f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7772f-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7772f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7772f-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="7772f-120">INPUTS</span></span>

### <span data-ttu-id="7772f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="7772f-121">System.String</span></span>

## <span data-ttu-id="7772f-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="7772f-122">OUTPUTS</span></span>

### <span data-ttu-id="7772f-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="7772f-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="7772f-124">Notas</span><span class="sxs-lookup"><span data-stu-id="7772f-124">NOTES</span></span>

## <span data-ttu-id="7772f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7772f-125">RELATED LINKS</span></span>
