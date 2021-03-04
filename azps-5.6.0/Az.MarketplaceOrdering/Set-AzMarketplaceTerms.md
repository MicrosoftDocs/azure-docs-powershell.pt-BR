---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885427"
---
# <span data-ttu-id="ec4de-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ec4de-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="ec4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4de-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4de-103">Aceitar ou rejeitar termos para um determinado publisher id(Publisher), id(Product) e plan id(Name).</span><span class="sxs-lookup"><span data-stu-id="ec4de-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ec4de-104">Use o Get-AzMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="ec4de-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="ec4de-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ec4de-105">SYNTAX</span></span>

### <span data-ttu-id="ec4de-106">AgreementAcceptParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ec4de-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4de-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec4de-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4de-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec4de-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4de-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec4de-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4de-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ec4de-110">DESCRIPTION</span></span>
<span data-ttu-id="ec4de-111">O cmdlet **Set-AzMarketplaceTerms** salva o objeto terms para determinado id(Publisher), id(Product) de oferta e planejar a tupla id(Name).</span><span class="sxs-lookup"><span data-stu-id="ec4de-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ec4de-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec4de-112">EXAMPLES</span></span>

### <span data-ttu-id="ec4de-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec4de-113">Example 1</span></span>
<span data-ttu-id="ec4de-114">Obter o contrato do editor do marketplace</span><span class="sxs-lookup"><span data-stu-id="ec4de-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="ec4de-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ec4de-115">Example 2</span></span>
<span data-ttu-id="ec4de-116">De definir o contrato de editor como "Aceitar".</span><span class="sxs-lookup"><span data-stu-id="ec4de-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="ec4de-117">Obter o valor do parâmetro 'Terms' do cmdlet 'Get-AzMarketplaceTerms'</span><span class="sxs-lookup"><span data-stu-id="ec4de-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="ec4de-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ec4de-118">PARAMETERS</span></span>

### <span data-ttu-id="ec4de-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="ec4de-119">-Accept</span></span>
<span data-ttu-id="ec4de-120">Passe isso para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="ec4de-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4de-121">-DefaultProfile</span></span>
<span data-ttu-id="ec4de-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ec4de-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec4de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec4de-123">-InputObject</span></span>
<span data-ttu-id="ec4de-124">Objeto Terms retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4de-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ec4de-125">Este é um parâmetro obrigatório se o parâmetro Accepted for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="ec4de-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ec4de-126">-Name</span></span>
<span data-ttu-id="ec4de-127">Planejar a cadeia de caracteres de identificador da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="ec4de-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-128">-Product</span><span class="sxs-lookup"><span data-stu-id="ec4de-128">-Product</span></span>
<span data-ttu-id="ec4de-129">Oferecer cadeia de caracteres de identificador de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="ec4de-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ec4de-130">-Publisher</span></span>
<span data-ttu-id="ec4de-131">Cadeia de caracteres de identificador do publisher da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="ec4de-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="ec4de-132">-Reject</span></span>
<span data-ttu-id="ec4de-133">Passe isso para rejeitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="ec4de-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-134">-Terms</span><span class="sxs-lookup"><span data-stu-id="ec4de-134">-Terms</span></span>
<span data-ttu-id="ec4de-135">Objeto Terms retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4de-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ec4de-136">Este é um parâmetro obrigatório se o parâmetro Accepted for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="ec4de-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec4de-137">-Confirm</span></span>
<span data-ttu-id="ec4de-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4de-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4de-139">-WhatIf</span></span>
<span data-ttu-id="ec4de-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec4de-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec4de-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec4de-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4de-142">CommonParameters</span></span>
<span data-ttu-id="ec4de-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4de-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec4de-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4de-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec4de-145">INPUTS</span></span>

### <span data-ttu-id="ec4de-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ec4de-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ec4de-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ec4de-147">OUTPUTS</span></span>

### <span data-ttu-id="ec4de-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ec4de-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ec4de-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="ec4de-149">NOTES</span></span>

## <span data-ttu-id="ec4de-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec4de-150">RELATED LINKS</span></span>
