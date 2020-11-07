---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944775"
---
# <span data-ttu-id="fa317-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fa317-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="fa317-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa317-102">SYNOPSIS</span></span>
<span data-ttu-id="fa317-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa317-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="fa317-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa317-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa317-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa317-105">DESCRIPTION</span></span>
<span data-ttu-id="fa317-106">O cmdlet **New-AzApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa317-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="fa317-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa317-107">EXAMPLES</span></span>

### <span data-ttu-id="fa317-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="fa317-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="fa317-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="fa317-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="fa317-110">OS</span><span class="sxs-lookup"><span data-stu-id="fa317-110">PARAMETERS</span></span>

### <span data-ttu-id="fa317-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="fa317-111">-Capacity</span></span>
<span data-ttu-id="fa317-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa317-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="fa317-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa317-113">-DefaultProfile</span></span>
<span data-ttu-id="fa317-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa317-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa317-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa317-115">-Name</span></span>
<span data-ttu-id="fa317-116">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="fa317-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="fa317-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fa317-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa317-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="fa317-118">Standard_Small</span></span>
- <span data-ttu-id="fa317-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="fa317-119">Standard_Medium</span></span>
- <span data-ttu-id="fa317-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="fa317-120">Standard_Large</span></span>
- <span data-ttu-id="fa317-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="fa317-121">WAF_Medium</span></span>
- <span data-ttu-id="fa317-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="fa317-122">WAF_Large</span></span>
- <span data-ttu-id="fa317-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="fa317-123">Standard_v2</span></span>
- <span data-ttu-id="fa317-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fa317-124">WAF_v2</span></span>

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

### <span data-ttu-id="fa317-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="fa317-125">-Tier</span></span>
<span data-ttu-id="fa317-126">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="fa317-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="fa317-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fa317-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa317-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="fa317-128">Standard</span></span>
- <span data-ttu-id="fa317-129">WAF</span><span class="sxs-lookup"><span data-stu-id="fa317-129">WAF</span></span>
- <span data-ttu-id="fa317-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="fa317-130">Standard_v2</span></span>
- <span data-ttu-id="fa317-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fa317-131">WAF_v2</span></span>

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

### <span data-ttu-id="fa317-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa317-132">CommonParameters</span></span>
<span data-ttu-id="fa317-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa317-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa317-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa317-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa317-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa317-135">INPUTS</span></span>

### <span data-ttu-id="fa317-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fa317-136">None</span></span>

## <span data-ttu-id="fa317-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa317-137">OUTPUTS</span></span>

### <span data-ttu-id="fa317-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fa317-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="fa317-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa317-139">NOTES</span></span>

## <span data-ttu-id="fa317-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa317-140">RELATED LINKS</span></span>

[<span data-ttu-id="fa317-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fa317-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="fa317-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="fa317-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


