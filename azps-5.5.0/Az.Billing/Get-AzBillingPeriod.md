---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116592"
---
# <span data-ttu-id="ce73b-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ce73b-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="ce73b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce73b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce73b-103">Obter períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce73b-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="ce73b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce73b-104">SYNTAX</span></span>

### <span data-ttu-id="ce73b-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ce73b-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce73b-106">Único</span><span class="sxs-lookup"><span data-stu-id="ce73b-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce73b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce73b-107">DESCRIPTION</span></span>
<span data-ttu-id="ce73b-108">O **cmdlet Get-AzBillingPeriod** obtém períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce73b-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="ce73b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce73b-109">EXAMPLES</span></span>

### <span data-ttu-id="ce73b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce73b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="ce73b-111">Obter todos os períodos de cobrança disponíveis da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce73b-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="ce73b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce73b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="ce73b-113">Obter o período de cobrança da assinatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ce73b-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="ce73b-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce73b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="ce73b-115">Obter no máximo dois períodos de cobrança da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce73b-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="ce73b-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce73b-116">PARAMETERS</span></span>

### <span data-ttu-id="ce73b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce73b-117">-DefaultProfile</span></span>
<span data-ttu-id="ce73b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ce73b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce73b-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ce73b-119">-MaxCount</span></span>
<span data-ttu-id="ce73b-120">Determine o número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="ce73b-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="ce73b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce73b-121">-Name</span></span>
<span data-ttu-id="ce73b-122">Nome de um período de cobrança específico para obter.</span><span class="sxs-lookup"><span data-stu-id="ce73b-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="ce73b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce73b-123">CommonParameters</span></span>
<span data-ttu-id="ce73b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce73b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce73b-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce73b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce73b-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="ce73b-126">INPUTS</span></span>

### <span data-ttu-id="ce73b-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ce73b-127">None</span></span>

## <span data-ttu-id="ce73b-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ce73b-128">OUTPUTS</span></span>

### <span data-ttu-id="ce73b-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="ce73b-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="ce73b-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ce73b-130">NOTES</span></span>

## <span data-ttu-id="ce73b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce73b-131">RELATED LINKS</span></span>
