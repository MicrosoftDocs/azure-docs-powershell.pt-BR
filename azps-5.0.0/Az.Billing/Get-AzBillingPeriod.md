---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118427"
---
# <span data-ttu-id="ec9c4-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ec9c4-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="ec9c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9c4-103">Obter períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="ec9c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec9c4-104">SYNTAX</span></span>

### <span data-ttu-id="ec9c4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec9c4-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec9c4-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="ec9c4-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec9c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec9c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ec9c4-108">O cmdlet **Get-AzBillingPeriod** Obtém períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="ec9c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec9c4-109">EXAMPLES</span></span>

### <span data-ttu-id="ec9c4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec9c4-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="ec9c4-111">Obtenha todos os períodos de cobrança disponíveis da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="ec9c4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ec9c4-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="ec9c4-113">Obter o período de cobrança da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="ec9c4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ec9c4-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="ec9c4-115">Obter no máximo 2 períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="ec9c4-116">OS</span><span class="sxs-lookup"><span data-stu-id="ec9c4-116">PARAMETERS</span></span>

### <span data-ttu-id="ec9c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9c4-117">-DefaultProfile</span></span>
<span data-ttu-id="ec9c4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ec9c4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec9c4-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ec9c4-119">-MaxCount</span></span>
<span data-ttu-id="ec9c4-120">Determine o número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="ec9c4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec9c4-121">-Name</span></span>
<span data-ttu-id="ec9c4-122">Nome de um período de cobrança específico para obter.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="ec9c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9c4-123">CommonParameters</span></span>
<span data-ttu-id="ec9c4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec9c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9c4-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9c4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9c4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec9c4-126">INPUTS</span></span>

### <span data-ttu-id="ec9c4-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ec9c4-127">None</span></span>

## <span data-ttu-id="ec9c4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec9c4-128">OUTPUTS</span></span>

### <span data-ttu-id="ec9c4-129">Microsoft. Azure. Commands. billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ec9c4-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="ec9c4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec9c4-130">NOTES</span></span>

## <span data-ttu-id="ec9c4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec9c4-131">RELATED LINKS</span></span>
