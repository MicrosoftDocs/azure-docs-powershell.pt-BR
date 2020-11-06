---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432798"
---
# <span data-ttu-id="84584-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="84584-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="84584-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84584-102">SYNOPSIS</span></span>
<span data-ttu-id="84584-103">Obter períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="84584-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84584-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84584-104">SYNTAX</span></span>

### <span data-ttu-id="84584-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="84584-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84584-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="84584-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84584-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84584-107">DESCRIPTION</span></span>
<span data-ttu-id="84584-108">O cmdlet **Get-AzureRmBillingPeriod** Obtém períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="84584-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="84584-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84584-109">EXAMPLES</span></span>

### <span data-ttu-id="84584-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84584-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="84584-111">Obtenha todos os períodos de cobrança disponíveis da assinatura.</span><span class="sxs-lookup"><span data-stu-id="84584-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="84584-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="84584-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="84584-113">Obter o período de cobrança da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="84584-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="84584-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="84584-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="84584-115">Obter no máximo 2 períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="84584-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="84584-116">OS</span><span class="sxs-lookup"><span data-stu-id="84584-116">PARAMETERS</span></span>

### <span data-ttu-id="84584-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84584-117">-DefaultProfile</span></span>
<span data-ttu-id="84584-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="84584-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84584-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="84584-119">-MaxCount</span></span>
<span data-ttu-id="84584-120">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="84584-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84584-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="84584-121">-Name</span></span>
<span data-ttu-id="84584-122">Nome de um período de cobrança específico para obter.</span><span class="sxs-lookup"><span data-stu-id="84584-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84584-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84584-123">CommonParameters</span></span>
<span data-ttu-id="84584-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84584-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84584-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84584-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84584-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84584-126">INPUTS</span></span>

### <span data-ttu-id="84584-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="84584-127">None</span></span>

## <span data-ttu-id="84584-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84584-128">OUTPUTS</span></span>

### <span data-ttu-id="84584-129">Microsoft. Azure. Commands. billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="84584-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="84584-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84584-130">NOTES</span></span>

## <span data-ttu-id="84584-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84584-131">RELATED LINKS</span></span>
