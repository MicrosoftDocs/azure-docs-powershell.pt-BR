---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114100"
---
# <span data-ttu-id="a090d-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a090d-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="a090d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a090d-102">SYNOPSIS</span></span>
<span data-ttu-id="a090d-103">Modifica a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="a090d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a090d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a090d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a090d-105">DESCRIPTION</span></span>
<span data-ttu-id="a090d-106">O cmdlet **Set-AzApplicationGatewaySku** modifica a unidade de manutenção de estoque (SKU) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="a090d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a090d-107">EXAMPLES</span></span>

### <span data-ttu-id="a090d-108">Exemplo 1: Atualizar a SKU do gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="a090d-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="a090d-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a090d-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a090d-110">O segundo comando atualiza a SKU do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="a090d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a090d-111">PARAMETERS</span></span>

### <span data-ttu-id="a090d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a090d-112">-ApplicationGateway</span></span>
<span data-ttu-id="a090d-113">Especifica o objeto do gateway de aplicativo com o qual este cmdlet associa a SKU.</span><span class="sxs-lookup"><span data-stu-id="a090d-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a090d-114">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="a090d-114">-Capacity</span></span>
<span data-ttu-id="a090d-115">Especifica a contagem de instâncias do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a090d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a090d-116">-DefaultProfile</span></span>
<span data-ttu-id="a090d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a090d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a090d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a090d-118">-Name</span></span>
<span data-ttu-id="a090d-119">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="a090d-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a090d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a090d-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="a090d-121">Standard_Small</span></span>
- <span data-ttu-id="a090d-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="a090d-122">Standard_Medium</span></span>
- <span data-ttu-id="a090d-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="a090d-123">Standard_Large</span></span>
- <span data-ttu-id="a090d-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="a090d-124">WAF_Medium</span></span>
- <span data-ttu-id="a090d-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="a090d-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a090d-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="a090d-126">-Tier</span></span>
<span data-ttu-id="a090d-127">Especifica o nível do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a090d-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="a090d-128">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a090d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a090d-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="a090d-129">Standard</span></span>
- <span data-ttu-id="a090d-130">Waf</span><span class="sxs-lookup"><span data-stu-id="a090d-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a090d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a090d-131">CommonParameters</span></span>
<span data-ttu-id="a090d-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a090d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a090d-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a090d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a090d-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="a090d-134">INPUTS</span></span>

### <span data-ttu-id="a090d-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a090d-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a090d-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="a090d-136">OUTPUTS</span></span>

### <span data-ttu-id="a090d-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a090d-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a090d-138">Notas</span><span class="sxs-lookup"><span data-stu-id="a090d-138">NOTES</span></span>

## <span data-ttu-id="a090d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a090d-139">RELATED LINKS</span></span>

[<span data-ttu-id="a090d-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a090d-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="a090d-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a090d-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


