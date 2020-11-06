---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441025"
---
# <span data-ttu-id="deec9-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="deec9-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="deec9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deec9-102">SYNOPSIS</span></span>
<span data-ttu-id="deec9-103">Aceitar ou rejeitar termos para um determinado ID de fornecedor (fornecedor), ID de oferta (produto) e ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="deec9-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="deec9-104">Use Get-AzureRmMarketplaceTerms para obter os termos do contrato.</span><span class="sxs-lookup"><span data-stu-id="deec9-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deec9-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deec9-105">SYNTAX</span></span>

### <span data-ttu-id="deec9-106">AgreementAcceptParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="deec9-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="deec9-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="deec9-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="deec9-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="deec9-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deec9-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="deec9-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deec9-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deec9-110">DESCRIPTION</span></span>
<span data-ttu-id="deec9-111">O cmdlet **set-AzureRmMarketplaceTerms** salva o objeto terms para a determinada ID de fornecedor (fornecedor), a ID de oferta (produto) e a tupla de ID de plano (nome).</span><span class="sxs-lookup"><span data-stu-id="deec9-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="deec9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deec9-112">EXAMPLES</span></span>

### <span data-ttu-id="deec9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="deec9-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="deec9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="deec9-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="deec9-115">OS</span><span class="sxs-lookup"><span data-stu-id="deec9-115">PARAMETERS</span></span>

### <span data-ttu-id="deec9-116">-Aceitar</span><span class="sxs-lookup"><span data-stu-id="deec9-116">-Accept</span></span>
<span data-ttu-id="deec9-117">Passe para aceitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="deec9-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deec9-118">-DefaultProfile</span></span>
<span data-ttu-id="deec9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deec9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="deec9-120">-InputObject</span></span>
<span data-ttu-id="deec9-121">Objeto termos retornado no Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deec9-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="deec9-122">Esse é um parâmetro obrigatório se o parâmetro aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="deec9-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="deec9-123">-Name</span></span>
<span data-ttu-id="deec9-124">Cadeia do identificador de plano da imagem que está sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="deec9-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-125">-Produto</span><span class="sxs-lookup"><span data-stu-id="deec9-125">-Product</span></span>
<span data-ttu-id="deec9-126">Cadeia de caracteres do identificador de oferta de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="deec9-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="deec9-127">-Publisher</span></span>
<span data-ttu-id="deec9-128">Identificador de editores cadeia de caracteres de imagem sendo implantada.</span><span class="sxs-lookup"><span data-stu-id="deec9-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-129">-Rejeitar</span><span class="sxs-lookup"><span data-stu-id="deec9-129">-Reject</span></span>
<span data-ttu-id="deec9-130">Passe para rejeitar os termos legais.</span><span class="sxs-lookup"><span data-stu-id="deec9-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-131">-Termos</span><span class="sxs-lookup"><span data-stu-id="deec9-131">-Terms</span></span>
<span data-ttu-id="deec9-132">Objeto termos retornado no Get-AzureRmMarketplaceTerms cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deec9-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="deec9-133">Esse é um parâmetro obrigatório se o parâmetro aceito for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="deec9-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="deec9-134">-Confirm</span></span>
<span data-ttu-id="deec9-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deec9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deec9-136">-WhatIf</span></span>
<span data-ttu-id="deec9-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="deec9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="deec9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deec9-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="deec9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deec9-139">CommonParameters</span></span>
<span data-ttu-id="deec9-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deec9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deec9-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deec9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deec9-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deec9-142">INPUTS</span></span>

### <span data-ttu-id="deec9-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="deec9-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="deec9-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="deec9-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="deec9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deec9-145">OUTPUTS</span></span>

### <span data-ttu-id="deec9-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="deec9-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="deec9-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="deec9-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="deec9-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deec9-148">NOTES</span></span>

## <span data-ttu-id="deec9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deec9-149">RELATED LINKS</span></span>

