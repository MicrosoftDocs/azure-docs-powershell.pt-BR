---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1f99fe982496fc6cef3ee9579d8e0be555880aaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892427"
---
# <span data-ttu-id="06409-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06409-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="06409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06409-102">SYNOPSIS</span></span>
<span data-ttu-id="06409-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06409-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="06409-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="06409-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06409-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="06409-105">DESCRIPTION</span></span>
<span data-ttu-id="06409-106">O cmdlet **New-AzApplicationGatewaySku** cria uma unidade de manutenção de ações (SKU) para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="06409-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="06409-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06409-107">EXAMPLES</span></span>

### <span data-ttu-id="06409-108">Exemplo 1: Criar uma SKU para um gateway de aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="06409-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="06409-109">Este comando cria uma SKU chamada Standard_Small para um gateway de aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="06409-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="06409-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="06409-110">PARAMETERS</span></span>

### <span data-ttu-id="06409-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="06409-111">-Capacity</span></span>
<span data-ttu-id="06409-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06409-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="06409-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06409-113">-DefaultProfile</span></span>
<span data-ttu-id="06409-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="06409-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06409-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06409-115">-Name</span></span>
<span data-ttu-id="06409-116">Especifica o nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="06409-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="06409-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="06409-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06409-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="06409-118">Standard_Small</span></span>
- <span data-ttu-id="06409-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="06409-119">Standard_Medium</span></span>
- <span data-ttu-id="06409-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="06409-120">Standard_Large</span></span>
- <span data-ttu-id="06409-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="06409-121">WAF_Medium</span></span>
- <span data-ttu-id="06409-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="06409-122">WAF_Large</span></span>
- <span data-ttu-id="06409-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="06409-123">Standard_v2</span></span>
- <span data-ttu-id="06409-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="06409-124">WAF_v2</span></span>

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

### <span data-ttu-id="06409-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="06409-125">-Tier</span></span>
<span data-ttu-id="06409-126">Especifica a camada do SKU.</span><span class="sxs-lookup"><span data-stu-id="06409-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="06409-127">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="06409-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06409-128">Standard</span><span class="sxs-lookup"><span data-stu-id="06409-128">Standard</span></span>
- <span data-ttu-id="06409-129">WAF</span><span class="sxs-lookup"><span data-stu-id="06409-129">WAF</span></span>
- <span data-ttu-id="06409-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="06409-130">Standard_v2</span></span>
- <span data-ttu-id="06409-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="06409-131">WAF_v2</span></span>

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

### <span data-ttu-id="06409-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06409-132">CommonParameters</span></span>
<span data-ttu-id="06409-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06409-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06409-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06409-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06409-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06409-135">INPUTS</span></span>

### <span data-ttu-id="06409-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06409-136">None</span></span>

## <span data-ttu-id="06409-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="06409-137">OUTPUTS</span></span>

### <span data-ttu-id="06409-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06409-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="06409-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="06409-139">NOTES</span></span>

## <span data-ttu-id="06409-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06409-140">RELATED LINKS</span></span>

[<span data-ttu-id="06409-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06409-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="06409-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06409-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


