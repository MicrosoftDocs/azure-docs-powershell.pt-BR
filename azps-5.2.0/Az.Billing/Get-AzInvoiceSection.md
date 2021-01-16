---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258667"
---
# <span data-ttu-id="9c906-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="9c906-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="9c906-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c906-102">SYNOPSIS</span></span>
<span data-ttu-id="9c906-103">Obter seções de fatura.</span><span class="sxs-lookup"><span data-stu-id="9c906-103">Get invoice sections.</span></span>

## <span data-ttu-id="9c906-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c906-104">SYNTAX</span></span>

### <span data-ttu-id="9c906-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="9c906-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c906-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="9c906-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c906-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c906-107">DESCRIPTION</span></span>
<span data-ttu-id="9c906-108">O cmdlet **Get-AzInvoiceSection** Obtém seções de fatura sob o perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="9c906-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="9c906-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c906-109">EXAMPLES</span></span>

### <span data-ttu-id="9c906-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c906-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="9c906-111">Obter todas as seções de fatura sob o perfil de cobrança especificado.</span><span class="sxs-lookup"><span data-stu-id="9c906-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="9c906-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c906-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="9c906-113">Obter a seção de fatura com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="9c906-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="9c906-114">OS</span><span class="sxs-lookup"><span data-stu-id="9c906-114">PARAMETERS</span></span>

### <span data-ttu-id="9c906-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c906-115">-DefaultProfile</span></span>
<span data-ttu-id="9c906-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9c906-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c906-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="9c906-117">-BillingAccountName</span></span>
<span data-ttu-id="9c906-118">Nome da conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="9c906-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="9c906-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="9c906-119">-BillingProfileName</span></span>
<span data-ttu-id="9c906-120">Nome do perfil de cobrança específico.</span><span class="sxs-lookup"><span data-stu-id="9c906-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="9c906-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c906-121">-Name</span></span>
<span data-ttu-id="9c906-122">Nome de uma seção de fatura específica.</span><span class="sxs-lookup"><span data-stu-id="9c906-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="9c906-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c906-123">CommonParameters</span></span>
<span data-ttu-id="9c906-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c906-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c906-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c906-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c906-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c906-126">INPUTS</span></span>

### <span data-ttu-id="9c906-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9c906-127">None</span></span>

## <span data-ttu-id="9c906-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c906-128">OUTPUTS</span></span>

### <span data-ttu-id="9c906-129">Microsoft. Azure. Commands. billing. Models. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="9c906-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="9c906-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c906-130">NOTES</span></span>

## <span data-ttu-id="9c906-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c906-131">RELATED LINKS</span></span>
