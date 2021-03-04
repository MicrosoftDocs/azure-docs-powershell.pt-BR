---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893401"
---
# <span data-ttu-id="00239-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="00239-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="00239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00239-102">SYNOPSIS</span></span>
<span data-ttu-id="00239-103">Obter seções de fatura.</span><span class="sxs-lookup"><span data-stu-id="00239-103">Get invoice sections.</span></span>

## <span data-ttu-id="00239-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="00239-104">SYNTAX</span></span>

### <span data-ttu-id="00239-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="00239-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00239-106">Single</span><span class="sxs-lookup"><span data-stu-id="00239-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00239-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="00239-107">DESCRIPTION</span></span>
<span data-ttu-id="00239-108">O cmdlet **Get-AzInvoiceSection** obtém seções de fatura no perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="00239-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="00239-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00239-109">EXAMPLES</span></span>

### <span data-ttu-id="00239-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00239-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="00239-111">Obter todas as seções de fatura no perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="00239-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="00239-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00239-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="00239-113">Obter a seção fatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="00239-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="00239-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="00239-114">PARAMETERS</span></span>

### <span data-ttu-id="00239-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00239-115">-DefaultProfile</span></span>
<span data-ttu-id="00239-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="00239-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00239-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="00239-117">-BillingAccountName</span></span>
<span data-ttu-id="00239-118">Nome da conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="00239-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="00239-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="00239-119">-BillingProfileName</span></span>
<span data-ttu-id="00239-120">Nome do perfil de cobrança específico.</span><span class="sxs-lookup"><span data-stu-id="00239-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="00239-121">-Name</span><span class="sxs-lookup"><span data-stu-id="00239-121">-Name</span></span>
<span data-ttu-id="00239-122">Nome de uma seção de fatura específica.</span><span class="sxs-lookup"><span data-stu-id="00239-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="00239-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00239-123">CommonParameters</span></span>
<span data-ttu-id="00239-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00239-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00239-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00239-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00239-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00239-126">INPUTS</span></span>

### <span data-ttu-id="00239-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="00239-127">None</span></span>

## <span data-ttu-id="00239-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="00239-128">OUTPUTS</span></span>

### <span data-ttu-id="00239-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="00239-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="00239-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="00239-130">NOTES</span></span>

## <span data-ttu-id="00239-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00239-131">RELATED LINKS</span></span>
