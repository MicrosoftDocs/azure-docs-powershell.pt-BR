---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: c66b3a2c4c151daf0a5d3df62aaaf248a7d2e338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889696"
---
# <span data-ttu-id="34b3d-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="34b3d-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="34b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="34b3d-103">Obter perfis de cobrança.</span><span class="sxs-lookup"><span data-stu-id="34b3d-103">Get billing profiles.</span></span>

## <span data-ttu-id="34b3d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34b3d-104">SYNTAX</span></span>

### <span data-ttu-id="34b3d-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34b3d-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34b3d-106">Single</span><span class="sxs-lookup"><span data-stu-id="34b3d-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34b3d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34b3d-107">DESCRIPTION</span></span>
<span data-ttu-id="34b3d-108">O cmdlet **Get-AzBillingProfile** obtém perfis de cobrança na conta de cobrança especificada.</span><span class="sxs-lookup"><span data-stu-id="34b3d-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="34b3d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="34b3d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34b3d-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="34b3d-111">Obter todos os perfis de cobrança na conta de cobrança especificada.</span><span class="sxs-lookup"><span data-stu-id="34b3d-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="34b3d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="34b3d-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="34b3d-113">Obter o perfil de cobrança com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="34b3d-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="34b3d-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="34b3d-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="34b3d-115">Obter todos os perfis de cobrança em conta de cobrança especificada e incluir as seções de fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="34b3d-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="34b3d-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="34b3d-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="34b3d-117">Obter o perfil de cobrança com o nome especificado e incluir as seções de fatura no resultado.</span><span class="sxs-lookup"><span data-stu-id="34b3d-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="34b3d-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34b3d-118">PARAMETERS</span></span>

### <span data-ttu-id="34b3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b3d-119">-DefaultProfile</span></span>
<span data-ttu-id="34b3d-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="34b3d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34b3d-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="34b3d-121">-BillingAccountName</span></span>
<span data-ttu-id="34b3d-122">Nome da conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="34b3d-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="34b3d-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="34b3d-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="34b3d-124">Inclua as seções de faturas no perfil de cobrança.</span><span class="sxs-lookup"><span data-stu-id="34b3d-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="34b3d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="34b3d-125">-Name</span></span>
<span data-ttu-id="34b3d-126">Nome de um perfil de cobrança específico.</span><span class="sxs-lookup"><span data-stu-id="34b3d-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="34b3d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b3d-127">CommonParameters</span></span>
<span data-ttu-id="34b3d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b3d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b3d-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b3d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b3d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34b3d-130">INPUTS</span></span>

### <span data-ttu-id="34b3d-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="34b3d-131">None</span></span>

## <span data-ttu-id="34b3d-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34b3d-132">OUTPUTS</span></span>

### <span data-ttu-id="34b3d-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="34b3d-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="34b3d-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="34b3d-134">NOTES</span></span>

## <span data-ttu-id="34b3d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34b3d-135">RELATED LINKS</span></span>
