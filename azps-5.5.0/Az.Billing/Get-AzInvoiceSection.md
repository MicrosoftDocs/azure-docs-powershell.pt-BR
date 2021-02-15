---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112214"
---
# <span data-ttu-id="0d008-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0d008-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="0d008-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d008-102">SYNOPSIS</span></span>
<span data-ttu-id="0d008-103">Obter seções de fatura.</span><span class="sxs-lookup"><span data-stu-id="0d008-103">Get invoice sections.</span></span>

## <span data-ttu-id="0d008-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d008-104">SYNTAX</span></span>

### <span data-ttu-id="0d008-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d008-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d008-106">Único</span><span class="sxs-lookup"><span data-stu-id="0d008-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d008-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d008-107">DESCRIPTION</span></span>
<span data-ttu-id="0d008-108">O **cmdlet Get-AzInvoiceSection obtém** seções de fatura sob o perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="0d008-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="0d008-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d008-109">EXAMPLES</span></span>

### <span data-ttu-id="0d008-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0d008-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="0d008-111">Obter todas as seções da fatura sob o perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="0d008-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="0d008-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0d008-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="0d008-113">Obter a seção da fatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="0d008-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="0d008-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d008-114">PARAMETERS</span></span>

### <span data-ttu-id="0d008-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d008-115">-DefaultProfile</span></span>
<span data-ttu-id="0d008-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0d008-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d008-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="0d008-117">-BillingAccountName</span></span>
<span data-ttu-id="0d008-118">Nome da conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="0d008-118">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d008-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="0d008-119">-BillingProfileName</span></span>
<span data-ttu-id="0d008-120">Nome do perfil de cobrança específico.</span><span class="sxs-lookup"><span data-stu-id="0d008-120">Name of the specific billing profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d008-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d008-121">-Name</span></span>
<span data-ttu-id="0d008-122">Nome de uma seção de fatura específica.</span><span class="sxs-lookup"><span data-stu-id="0d008-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="0d008-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d008-123">CommonParameters</span></span>
<span data-ttu-id="0d008-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d008-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d008-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d008-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d008-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d008-126">INPUTS</span></span>

### <span data-ttu-id="0d008-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0d008-127">None</span></span>

## <span data-ttu-id="0d008-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d008-128">OUTPUTS</span></span>

### <span data-ttu-id="0d008-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="0d008-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="0d008-130">Notas</span><span class="sxs-lookup"><span data-stu-id="0d008-130">NOTES</span></span>

## <span data-ttu-id="0d008-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d008-131">RELATED LINKS</span></span>
