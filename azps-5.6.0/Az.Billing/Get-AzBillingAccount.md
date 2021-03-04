---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886359"
---
# <span data-ttu-id="6e5a8-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6e5a8-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="6e5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5a8-103">Obter contas de cobrança.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-103">Get billing accounts.</span></span>

## <span data-ttu-id="6e5a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e5a8-104">SYNTAX</span></span>

### <span data-ttu-id="6e5a8-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e5a8-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e5a8-106">Single</span><span class="sxs-lookup"><span data-stu-id="6e5a8-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e5a8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e5a8-107">DESCRIPTION</span></span>
<span data-ttu-id="6e5a8-108">O cmdlet **Get-AzBillingAccount** obtém contas de cobrança, o usuário tem acesso.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="6e5a8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-109">EXAMPLES</span></span>

### <span data-ttu-id="6e5a8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e5a8-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="6e5a8-111">Obter todas as contas de cobrança que o usuário tem acesso.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="6e5a8-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6e5a8-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6e5a8-113">Obter a conta de cobrança com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="6e5a8-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6e5a8-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="6e5a8-115">Obter todas as contas de cobrança que o usuário tem acesso e incluir o endereço no resultado.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="6e5a8-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="6e5a8-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="6e5a8-117">Obter todas as contas de cobrança que o usuário tem acesso e incluir os perfis de cobrança no resultado.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="6e5a8-118">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="6e5a8-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="6e5a8-119">Obter todas as contas de cobrança às que o usuário tem acesso e inclua os perfis de cobrança e as seções de fatura abaixo delas no resultado.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="6e5a8-120">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="6e5a8-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6e5a8-121">Obter a conta de cobrança com o nome especificado e incluir o endereço, perfis de cobrança e seções de fatura sob eles no resultado.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="6e5a8-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-122">PARAMETERS</span></span>

### <span data-ttu-id="6e5a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5a8-123">-DefaultProfile</span></span>
<span data-ttu-id="6e5a8-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6e5a8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e5a8-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="6e5a8-125">-IncludeAddress</span></span>
<span data-ttu-id="6e5a8-126">Inclua o endereço da conta de cobrança.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="6e5a8-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="6e5a8-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="6e5a8-128">Inclua os perfis de cobrança na conta de cobrança.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="6e5a8-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="6e5a8-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="6e5a8-130">Inclua os perfis de cobrança em contas de cobrança e seções de faturas abaixo deles.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="6e5a8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6e5a8-131">-Name</span></span>
<span data-ttu-id="6e5a8-132">Nome de uma conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="6e5a8-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="6e5a8-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="6e5a8-134">Listar as entidades de cobrança em conta de cobrança que podem ser usadas como entrada para criar assinatura.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e5a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5a8-135">CommonParameters</span></span>
<span data-ttu-id="6e5a8-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5a8-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5a8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5a8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-138">INPUTS</span></span>

### <span data-ttu-id="6e5a8-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6e5a8-139">None</span></span>

## <span data-ttu-id="6e5a8-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-140">OUTPUTS</span></span>

### <span data-ttu-id="6e5a8-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="6e5a8-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="6e5a8-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e5a8-142">NOTES</span></span>

## <span data-ttu-id="6e5a8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e5a8-143">RELATED LINKS</span></span>
