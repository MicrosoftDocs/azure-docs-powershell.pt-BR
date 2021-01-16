---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259338"
---
# <span data-ttu-id="7b2b7-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="7b2b7-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="7b2b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2b7-103">Obter perfis de cobrança.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-103">Get billing profiles.</span></span>

## <span data-ttu-id="7b2b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b2b7-104">SYNTAX</span></span>

### <span data-ttu-id="7b2b7-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b2b7-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b2b7-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="7b2b7-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b2b7-107">DESCRIPTION</span></span>
<span data-ttu-id="7b2b7-108">O cmdlet **Get-AzBillingProfile** Obtém perfis de cobrança na conta de cobrança especificada.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="7b2b7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b2b7-109">EXAMPLES</span></span>

### <span data-ttu-id="7b2b7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b2b7-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="7b2b7-111">Obter todos os perfis de cobrança na conta de cobrança especificada.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="7b2b7-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7b2b7-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="7b2b7-113">Obter o perfil de cobrança com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="7b2b7-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7b2b7-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="7b2b7-115">Obter todos os perfis de cobrança na conta de cobrança especificada e incluir as seções de fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="7b2b7-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7b2b7-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="7b2b7-117">Obter o perfil de cobrança com o nome especificado e incluir as seções de fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="7b2b7-118">OS</span><span class="sxs-lookup"><span data-stu-id="7b2b7-118">PARAMETERS</span></span>

### <span data-ttu-id="7b2b7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2b7-119">-DefaultProfile</span></span>
<span data-ttu-id="7b2b7-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7b2b7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b2b7-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="7b2b7-121">-BillingAccountName</span></span>
<span data-ttu-id="7b2b7-122">Nome da conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="7b2b7-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="7b2b7-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="7b2b7-124">Inclua as seções faturas em perfil de cobrança.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-124">Include the invoices sections under billing profile.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2b7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b2b7-125">-Name</span></span>
<span data-ttu-id="7b2b7-126">Nome de um perfil de cobrança específico.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="7b2b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2b7-127">CommonParameters</span></span>
<span data-ttu-id="7b2b7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2b7-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2b7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2b7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b2b7-130">INPUTS</span></span>

### <span data-ttu-id="7b2b7-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b2b7-131">None</span></span>

## <span data-ttu-id="7b2b7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b2b7-132">OUTPUTS</span></span>

### <span data-ttu-id="7b2b7-133">Microsoft. Azure. Commands. billing. Models. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="7b2b7-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="7b2b7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b2b7-134">NOTES</span></span>

## <span data-ttu-id="7b2b7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b2b7-135">RELATED LINKS</span></span>
