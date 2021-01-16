---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262459"
---
# <span data-ttu-id="ba4ce-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba4ce-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="ba4ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4ce-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="ba4ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba4ce-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba4ce-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4ce-106">O cmdlet **New-AzApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="ba4ce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba4ce-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4ce-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="ba4ce-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="ba4ce-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="ba4ce-110">OS</span><span class="sxs-lookup"><span data-stu-id="ba4ce-110">PARAMETERS</span></span>

### <span data-ttu-id="ba4ce-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="ba4ce-111">-Capacity</span></span>
<span data-ttu-id="ba4ce-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="ba4ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4ce-113">-DefaultProfile</span></span>
<span data-ttu-id="ba4ce-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4ce-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba4ce-115">-Name</span></span>
<span data-ttu-id="ba4ce-116">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="ba4ce-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ba4ce-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba4ce-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="ba4ce-118">Standard_Small</span></span>
- <span data-ttu-id="ba4ce-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="ba4ce-119">Standard_Medium</span></span>
- <span data-ttu-id="ba4ce-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="ba4ce-120">Standard_Large</span></span>
- <span data-ttu-id="ba4ce-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="ba4ce-121">WAF_Medium</span></span>
- <span data-ttu-id="ba4ce-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="ba4ce-122">WAF_Large</span></span>
- <span data-ttu-id="ba4ce-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="ba4ce-123">Standard_v2</span></span>
- <span data-ttu-id="ba4ce-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ba4ce-124">WAF_v2</span></span>

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

### <span data-ttu-id="ba4ce-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="ba4ce-125">-Tier</span></span>
<span data-ttu-id="ba4ce-126">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="ba4ce-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ba4ce-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba4ce-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="ba4ce-128">Standard</span></span>
- <span data-ttu-id="ba4ce-129">WAF</span><span class="sxs-lookup"><span data-stu-id="ba4ce-129">WAF</span></span>
- <span data-ttu-id="ba4ce-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="ba4ce-130">Standard_v2</span></span>
- <span data-ttu-id="ba4ce-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ba4ce-131">WAF_v2</span></span>

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

### <span data-ttu-id="ba4ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4ce-132">CommonParameters</span></span>
<span data-ttu-id="ba4ce-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4ce-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4ce-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4ce-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba4ce-135">INPUTS</span></span>

### <span data-ttu-id="ba4ce-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ba4ce-136">None</span></span>

## <span data-ttu-id="ba4ce-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba4ce-137">OUTPUTS</span></span>

### <span data-ttu-id="ba4ce-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba4ce-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="ba4ce-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba4ce-139">NOTES</span></span>

## <span data-ttu-id="ba4ce-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba4ce-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba4ce-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba4ce-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="ba4ce-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba4ce-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


