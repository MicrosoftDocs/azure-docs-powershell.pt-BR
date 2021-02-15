---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111781"
---
# <span data-ttu-id="7af1d-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="7af1d-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="7af1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7af1d-102">SYNOPSIS</span></span>
<span data-ttu-id="7af1d-103">Aceitar ou rejeitar termos para uma determinada ID do publisher(Publisher), id da oferta(Produto) e id do plano(Nome).</span><span class="sxs-lookup"><span data-stu-id="7af1d-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="7af1d-104">Use o Get-AzMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="7af1d-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="7af1d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7af1d-105">SYNTAX</span></span>

### <span data-ttu-id="7af1d-106">AgreementAcceptParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7af1d-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7af1d-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7af1d-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7af1d-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="7af1d-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7af1d-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7af1d-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7af1d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7af1d-110">DESCRIPTION</span></span>
<span data-ttu-id="7af1d-111">O cmdlet **Set-AzMarketplaceTerms** salva o objeto de termos para determinada id do publisher(Publisher), id da oferta(Produto) e id do plano(Nome) da tupla.</span><span class="sxs-lookup"><span data-stu-id="7af1d-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="7af1d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7af1d-112">EXAMPLES</span></span>

### <span data-ttu-id="7af1d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7af1d-113">Example 1</span></span>
<span data-ttu-id="7af1d-114">Obter o contrato do editor do marketplace</span><span class="sxs-lookup"><span data-stu-id="7af1d-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="7af1d-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7af1d-115">Example 2</span></span>
<span data-ttu-id="7af1d-116">De definir o contrato do editor como "Aceitar".</span><span class="sxs-lookup"><span data-stu-id="7af1d-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="7af1d-117">Obter o valor do parâmetro 'Termos' do cmdlet 'Get-AzMarketplaceTerms'</span><span class="sxs-lookup"><span data-stu-id="7af1d-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="7af1d-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7af1d-118">PARAMETERS</span></span>

### <span data-ttu-id="7af1d-119">-Aceitar</span><span class="sxs-lookup"><span data-stu-id="7af1d-119">-Accept</span></span>
<span data-ttu-id="7af1d-120">Passe isso para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="7af1d-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="7af1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af1d-121">-DefaultProfile</span></span>
<span data-ttu-id="7af1d-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7af1d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af1d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7af1d-123">-InputObject</span></span>
<span data-ttu-id="7af1d-124">Objeto Termos retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af1d-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7af1d-125">Esse é um parâmetro obrigatório se o parâmetro Aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7af1d-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="7af1d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7af1d-126">-Name</span></span>
<span data-ttu-id="7af1d-127">Cadeia de caracteres identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="7af1d-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7af1d-128">-Produto</span><span class="sxs-lookup"><span data-stu-id="7af1d-128">-Product</span></span>
<span data-ttu-id="7af1d-129">Oferecer cadeia de caracteres identificador da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="7af1d-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7af1d-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7af1d-130">-Publisher</span></span>
<span data-ttu-id="7af1d-131">Cadeia de caracteres identificador do Publisher da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="7af1d-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="7af1d-132">-Rejeitar</span><span class="sxs-lookup"><span data-stu-id="7af1d-132">-Reject</span></span>
<span data-ttu-id="7af1d-133">Passe isso para rejeitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="7af1d-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="7af1d-134">-Termos</span><span class="sxs-lookup"><span data-stu-id="7af1d-134">-Terms</span></span>
<span data-ttu-id="7af1d-135">Objeto Termos retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af1d-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="7af1d-136">Esse é um parâmetro obrigatório se o parâmetro Aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7af1d-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="7af1d-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7af1d-137">-Confirm</span></span>
<span data-ttu-id="7af1d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af1d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7af1d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7af1d-139">-WhatIf</span></span>
<span data-ttu-id="7af1d-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7af1d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7af1d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7af1d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7af1d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af1d-142">CommonParameters</span></span>
<span data-ttu-id="7af1d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af1d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af1d-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af1d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af1d-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="7af1d-145">INPUTS</span></span>

### <span data-ttu-id="7af1d-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7af1d-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7af1d-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="7af1d-147">OUTPUTS</span></span>

### <span data-ttu-id="7af1d-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="7af1d-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="7af1d-149">Notas</span><span class="sxs-lookup"><span data-stu-id="7af1d-149">NOTES</span></span>

## <span data-ttu-id="7af1d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7af1d-150">RELATED LINKS</span></span>
