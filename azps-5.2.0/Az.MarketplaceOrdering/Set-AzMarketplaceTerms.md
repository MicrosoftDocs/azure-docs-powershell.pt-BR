---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257687"
---
# <span data-ttu-id="2c6a8-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="2c6a8-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="2c6a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6a8-103">Aceitar ou rejeitar termos para um determinado ID de fornecedor (fornecedor), ID de oferta (produto) e ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="2c6a8-104">Use Get-AzMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="2c6a8-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c6a8-105">SYNTAX</span></span>

### <span data-ttu-id="2c6a8-106">AgreementAcceptParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c6a8-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c6a8-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6a8-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c6a8-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6a8-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c6a8-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6a8-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c6a8-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c6a8-110">DESCRIPTION</span></span>
<span data-ttu-id="2c6a8-111">O cmdlet **set-AzMarketplaceTerms** salva o objeto terms para a determinada ID de fornecedor (fornecedor), a ID de oferta (produto) e a tupla de ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="2c6a8-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="2c6a8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c6a8-112">EXAMPLES</span></span>

### <span data-ttu-id="2c6a8-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c6a8-113">Example 1</span></span>
<span data-ttu-id="2c6a8-114">Obter o contrato de fornecedor do Marketplace</span><span class="sxs-lookup"><span data-stu-id="2c6a8-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="2c6a8-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2c6a8-115">Example 2</span></span>
<span data-ttu-id="2c6a8-116">Defina o contrato de fornecedor como ' Aceito '.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="2c6a8-117">Obter o valor para o parâmetro "termos" do cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="2c6a8-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="2c6a8-118">OS</span><span class="sxs-lookup"><span data-stu-id="2c6a8-118">PARAMETERS</span></span>

### <span data-ttu-id="2c6a8-119">-Aceitar</span><span class="sxs-lookup"><span data-stu-id="2c6a8-119">-Accept</span></span>
<span data-ttu-id="2c6a8-120">Passe para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="2c6a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6a8-121">-DefaultProfile</span></span>
<span data-ttu-id="2c6a8-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c6a8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c6a8-123">-InputObject</span></span>
<span data-ttu-id="2c6a8-124">Objeto termos retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2c6a8-125">Esse é um parâmetro obrigatório se o parâmetro aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="2c6a8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c6a8-126">-Name</span></span>
<span data-ttu-id="2c6a8-127">Cadeia do identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="2c6a8-128">-Produto</span><span class="sxs-lookup"><span data-stu-id="2c6a8-128">-Product</span></span>
<span data-ttu-id="2c6a8-129">Cadeia de caracteres do identificador de oferta de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="2c6a8-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2c6a8-130">-Publisher</span></span>
<span data-ttu-id="2c6a8-131">Identificador de editores cadeia de caracteres de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="2c6a8-132">-Rejeitar</span><span class="sxs-lookup"><span data-stu-id="2c6a8-132">-Reject</span></span>
<span data-ttu-id="2c6a8-133">Passe para rejeitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="2c6a8-134">-Termos</span><span class="sxs-lookup"><span data-stu-id="2c6a8-134">-Terms</span></span>
<span data-ttu-id="2c6a8-135">Objeto termos retornado no Get-AzMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2c6a8-136">Esse é um parâmetro obrigatório se o parâmetro aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="2c6a8-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c6a8-137">-Confirm</span></span>
<span data-ttu-id="2c6a8-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c6a8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c6a8-139">-WhatIf</span></span>
<span data-ttu-id="2c6a8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c6a8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c6a8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6a8-142">CommonParameters</span></span>
<span data-ttu-id="2c6a8-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c6a8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6a8-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6a8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6a8-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c6a8-145">INPUTS</span></span>

### <span data-ttu-id="2c6a8-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2c6a8-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2c6a8-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c6a8-147">OUTPUTS</span></span>

### <span data-ttu-id="2c6a8-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2c6a8-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2c6a8-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c6a8-149">NOTES</span></span>

## <span data-ttu-id="2c6a8-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c6a8-150">RELATED LINKS</span></span>
