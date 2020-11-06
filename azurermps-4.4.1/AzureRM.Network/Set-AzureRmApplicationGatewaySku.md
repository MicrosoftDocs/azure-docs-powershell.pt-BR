---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430720"
---
# <span data-ttu-id="4ab92-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ab92-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="4ab92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ab92-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab92-103">Modifica a SKU de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ab92-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ab92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ab92-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ab92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ab92-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab92-106">O cmdlet **set-AzureRmApplicationGatewaySku** modifica a SKU (unidade de manutenção de estoque) de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ab92-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="4ab92-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ab92-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab92-108">Exemplo 1: atualizar o SKU do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4ab92-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="4ab92-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4ab92-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4ab92-110">O segundo comando atualiza a SKU do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ab92-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="4ab92-111">OS</span><span class="sxs-lookup"><span data-stu-id="4ab92-111">PARAMETERS</span></span>

### <span data-ttu-id="4ab92-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ab92-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ab92-113">Especifica o objeto do gateway do aplicativo com o qual esse cmdlet associa a SKU.</span><span class="sxs-lookup"><span data-stu-id="4ab92-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="4ab92-114">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="4ab92-114">-Capacity</span></span>
<span data-ttu-id="4ab92-115">Especifica a contagem de instâncias do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ab92-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab92-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ab92-116">-Name</span></span>
<span data-ttu-id="4ab92-117">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ab92-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="4ab92-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4ab92-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ab92-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="4ab92-119">Standard_Small</span></span>
- <span data-ttu-id="4ab92-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="4ab92-120">Standard_Medium</span></span>
- <span data-ttu-id="4ab92-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="4ab92-121">Standard_Large</span></span>
- <span data-ttu-id="4ab92-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="4ab92-122">WAF_Medium</span></span>
- <span data-ttu-id="4ab92-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="4ab92-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab92-124">-Tier</span><span class="sxs-lookup"><span data-stu-id="4ab92-124">-Tier</span></span>
<span data-ttu-id="4ab92-125">Especifica a camada do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ab92-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="4ab92-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4ab92-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ab92-127">Oficial</span><span class="sxs-lookup"><span data-stu-id="4ab92-127">Standard</span></span>
- <span data-ttu-id="4ab92-128">WAF</span><span class="sxs-lookup"><span data-stu-id="4ab92-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab92-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab92-129">-DefaultProfile</span></span>
<span data-ttu-id="4ab92-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab92-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab92-131">CommonParameters</span></span>
<span data-ttu-id="4ab92-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab92-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab92-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab92-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ab92-134">INPUTS</span></span>

### <span data-ttu-id="4ab92-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab92-135">System.String</span></span>

## <span data-ttu-id="4ab92-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ab92-136">OUTPUTS</span></span>

### <span data-ttu-id="4ab92-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ab92-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ab92-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ab92-138">NOTES</span></span>

## <span data-ttu-id="4ab92-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ab92-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ab92-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ab92-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="4ab92-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4ab92-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


