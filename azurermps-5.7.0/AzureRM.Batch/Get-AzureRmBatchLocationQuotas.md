---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 1390efccef67e6bfb626e9b31d1a58c72c9fb36e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609519"
---
# <span data-ttu-id="dc1a0-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="dc1a0-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="dc1a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1a0-103">Obtém as cotas de serviço em lotes para a sua assinatura em determinado local.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc1a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc1a0-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc1a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1a0-106">Obtém as cotas de serviço em lotes para a assinatura especificada em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="dc1a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc1a0-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1a0-108">Exemplo 1: obter as cotas de serviço em lotes para a assinatura na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="dc1a0-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="dc1a0-109">Este comando obtém as cotas para a assinatura atual na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="dc1a0-110">O valor de retorno indica que essa assinatura pode criar apenas uma conta em lotes nessa região.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="dc1a0-111">OS</span><span class="sxs-lookup"><span data-stu-id="dc1a0-111">PARAMETERS</span></span>

### <span data-ttu-id="dc1a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1a0-112">-DefaultProfile</span></span>
<span data-ttu-id="dc1a0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc1a0-114">-Local</span><span class="sxs-lookup"><span data-stu-id="dc1a0-114">-Location</span></span>
<span data-ttu-id="dc1a0-115">Especifica a região para a qual esse cmdlet verifica as cotas.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="dc1a0-116">Para obter mais informações, consulte regiões do Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="dc1a0-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc1a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1a0-117">CommonParameters</span></span>
<span data-ttu-id="dc1a0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1a0-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1a0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1a0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc1a0-120">INPUTS</span></span>

### <span data-ttu-id="dc1a0-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc1a0-121">None</span></span>
<span data-ttu-id="dc1a0-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="dc1a0-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc1a0-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc1a0-123">OUTPUTS</span></span>

### <span data-ttu-id="dc1a0-124">Microsoft.Azure.Commands.Batch. Modelos. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="dc1a0-124">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="dc1a0-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc1a0-125">NOTES</span></span>

## <span data-ttu-id="dc1a0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc1a0-126">RELATED LINKS</span></span>

