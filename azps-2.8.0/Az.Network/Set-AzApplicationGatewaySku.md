---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: ccc78a65041cac5cb471ac1f1bfa8d3ea3248ba1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772213"
---
# <span data-ttu-id="ab808-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ab808-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="ab808-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab808-102">SYNOPSIS</span></span>
<span data-ttu-id="ab808-103">Modifica a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab808-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="ab808-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab808-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab808-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab808-105">DESCRIPTION</span></span>
<span data-ttu-id="ab808-106">O cmdlet **set-AzApplicationGatewaySku** modifica a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab808-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="ab808-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab808-107">EXAMPLES</span></span>

### <span data-ttu-id="ab808-108">Exemplo 1: atualizar o SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ab808-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="ab808-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ab808-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ab808-110">O segundo comando atualiza a SKU do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab808-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="ab808-111">OS</span><span class="sxs-lookup"><span data-stu-id="ab808-111">PARAMETERS</span></span>

### <span data-ttu-id="ab808-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab808-112">-ApplicationGateway</span></span>
<span data-ttu-id="ab808-113">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa a SKU.</span><span class="sxs-lookup"><span data-stu-id="ab808-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="ab808-114">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="ab808-114">-Capacity</span></span>
<span data-ttu-id="ab808-115">Especifica a contagem de instâncias do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab808-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="ab808-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab808-116">-DefaultProfile</span></span>
<span data-ttu-id="ab808-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab808-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab808-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab808-118">-Name</span></span>
<span data-ttu-id="ab808-119">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab808-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="ab808-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ab808-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab808-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="ab808-121">Standard_Small</span></span>
- <span data-ttu-id="ab808-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="ab808-122">Standard_Medium</span></span>
- <span data-ttu-id="ab808-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="ab808-123">Standard_Large</span></span>
- <span data-ttu-id="ab808-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="ab808-124">WAF_Medium</span></span>
- <span data-ttu-id="ab808-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="ab808-125">WAF_Large</span></span>

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

### <span data-ttu-id="ab808-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="ab808-126">-Tier</span></span>
<span data-ttu-id="ab808-127">Especifica a camada do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ab808-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="ab808-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ab808-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ab808-129">Oficial</span><span class="sxs-lookup"><span data-stu-id="ab808-129">Standard</span></span>
- <span data-ttu-id="ab808-130">WAF</span><span class="sxs-lookup"><span data-stu-id="ab808-130">WAF</span></span>

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

### <span data-ttu-id="ab808-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab808-131">CommonParameters</span></span>
<span data-ttu-id="ab808-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab808-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab808-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab808-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab808-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab808-134">INPUTS</span></span>

### <span data-ttu-id="ab808-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab808-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab808-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab808-136">OUTPUTS</span></span>

### <span data-ttu-id="ab808-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab808-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab808-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab808-138">NOTES</span></span>

## <span data-ttu-id="ab808-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab808-139">RELATED LINKS</span></span>

[<span data-ttu-id="ab808-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ab808-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="ab808-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ab808-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


