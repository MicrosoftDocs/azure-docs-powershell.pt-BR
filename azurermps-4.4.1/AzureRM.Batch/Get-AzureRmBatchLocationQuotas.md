---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 208ba1055523a1dc76de88d665a7b1dbd097144e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430763"
---
# <span data-ttu-id="df23e-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="df23e-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="df23e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df23e-102">SYNOPSIS</span></span>
<span data-ttu-id="df23e-103">Obtém as cotas de serviço em lotes para a sua assinatura em determinado local.</span><span class="sxs-lookup"><span data-stu-id="df23e-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df23e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df23e-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df23e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df23e-105">DESCRIPTION</span></span>
<span data-ttu-id="df23e-106">Obtém as cotas de serviço em lotes para a assinatura especificada em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="df23e-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="df23e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df23e-107">EXAMPLES</span></span>

### <span data-ttu-id="df23e-108">Exemplo 1: obter as cotas de serviço em lotes para a assinatura na região oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="df23e-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="df23e-109">Este comando obtém as cotas para a assinatura atual na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="df23e-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="df23e-110">O valor de retorno indica que essa assinatura pode criar apenas uma conta em lotes nessa região.</span><span class="sxs-lookup"><span data-stu-id="df23e-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="df23e-111">OS</span><span class="sxs-lookup"><span data-stu-id="df23e-111">PARAMETERS</span></span>

### <span data-ttu-id="df23e-112">-Local</span><span class="sxs-lookup"><span data-stu-id="df23e-112">-Location</span></span>
<span data-ttu-id="df23e-113">Especifica a região para a qual esse cmdlet verifica as cotas.</span><span class="sxs-lookup"><span data-stu-id="df23e-113">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="df23e-114">Para obter mais informações, consulte regiões do Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="df23e-114">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="df23e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df23e-115">-DefaultProfile</span></span>
<span data-ttu-id="df23e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df23e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df23e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df23e-117">CommonParameters</span></span>
<span data-ttu-id="df23e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df23e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df23e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df23e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df23e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df23e-120">INPUTS</span></span>

## <span data-ttu-id="df23e-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df23e-121">OUTPUTS</span></span>

### <span data-ttu-id="df23e-122">Microsoft.Azure.Commands.Batch. Modelos. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="df23e-122">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="df23e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df23e-123">NOTES</span></span>

## <span data-ttu-id="df23e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df23e-124">RELATED LINKS</span></span>

