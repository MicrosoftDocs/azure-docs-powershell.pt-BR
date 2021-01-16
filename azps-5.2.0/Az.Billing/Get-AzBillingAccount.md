---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261250"
---
# <span data-ttu-id="53032-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="53032-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="53032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53032-102">SYNOPSIS</span></span>
<span data-ttu-id="53032-103">Obter contas de cobrança.</span><span class="sxs-lookup"><span data-stu-id="53032-103">Get billing accounts.</span></span>

## <span data-ttu-id="53032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53032-104">SYNTAX</span></span>

### <span data-ttu-id="53032-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="53032-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53032-106">Apenas</span><span class="sxs-lookup"><span data-stu-id="53032-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53032-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53032-107">DESCRIPTION</span></span>
<span data-ttu-id="53032-108">O cmdlet **Get-AzBillingAccount** Obtém contas de cobrança, o usuário tem acesso a.</span><span class="sxs-lookup"><span data-stu-id="53032-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="53032-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53032-109">EXAMPLES</span></span>

### <span data-ttu-id="53032-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53032-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="53032-111">Obter todas as contas de cobrança às quais o usuário tem acesso.</span><span class="sxs-lookup"><span data-stu-id="53032-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="53032-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="53032-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="53032-113">Obter a conta de cobrança com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="53032-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="53032-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="53032-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="53032-115">Obter todas as contas de cobrança às quais o usuário tem acesso e incluir o endereço no resultado.</span><span class="sxs-lookup"><span data-stu-id="53032-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="53032-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="53032-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="53032-117">Obter todas as contas de cobrança às quais o usuário tem acesso e incluir os perfis de cobrança no resultado.</span><span class="sxs-lookup"><span data-stu-id="53032-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="53032-118">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="53032-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="53032-119">Obter todas as contas de cobrança as quais o usuário tem acesso e incluir as seções perfis de cobrança e faturas sob elas no resultado.</span><span class="sxs-lookup"><span data-stu-id="53032-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="53032-120">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="53032-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="53032-121">Obtenha a conta de cobrança com o nome especificado e inclua o endereço, os perfis de cobrança e as seções de fatura sob eles no resultado.</span><span class="sxs-lookup"><span data-stu-id="53032-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="53032-122">OS</span><span class="sxs-lookup"><span data-stu-id="53032-122">PARAMETERS</span></span>

### <span data-ttu-id="53032-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53032-123">-DefaultProfile</span></span>
<span data-ttu-id="53032-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="53032-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53032-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="53032-125">-IncludeAddress</span></span>
<span data-ttu-id="53032-126">Inclua o endereço da conta de cobrança.</span><span class="sxs-lookup"><span data-stu-id="53032-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="53032-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="53032-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="53032-128">Inclua os perfis de cobrança na conta de cobrança.</span><span class="sxs-lookup"><span data-stu-id="53032-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="53032-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="53032-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="53032-130">Inclua os perfis de cobrança nas seções conta de cobrança e faturas.</span><span class="sxs-lookup"><span data-stu-id="53032-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="53032-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="53032-131">-Name</span></span>
<span data-ttu-id="53032-132">Nome de uma conta de cobrança específica.</span><span class="sxs-lookup"><span data-stu-id="53032-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="53032-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="53032-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="53032-134">Liste as entidades de cobrança em conta de cobrança que podem ser usadas como entrada para criar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="53032-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="53032-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53032-135">CommonParameters</span></span>
<span data-ttu-id="53032-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53032-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53032-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53032-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53032-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53032-138">INPUTS</span></span>

### <span data-ttu-id="53032-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53032-139">None</span></span>

## <span data-ttu-id="53032-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53032-140">OUTPUTS</span></span>

### <span data-ttu-id="53032-141">Microsoft. Azure. Commands. billing. Models. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="53032-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="53032-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53032-142">NOTES</span></span>

## <span data-ttu-id="53032-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53032-143">RELATED LINKS</span></span>
