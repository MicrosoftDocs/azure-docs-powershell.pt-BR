---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771657"
---
# <span data-ttu-id="c720c-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c720c-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="c720c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c720c-102">SYNOPSIS</span></span>
<span data-ttu-id="c720c-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c720c-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="c720c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c720c-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c720c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c720c-105">DESCRIPTION</span></span>
<span data-ttu-id="c720c-106">O cmdlet **New-AzApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c720c-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="c720c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c720c-107">EXAMPLES</span></span>

### <span data-ttu-id="c720c-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="c720c-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="c720c-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="c720c-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="c720c-110">OS</span><span class="sxs-lookup"><span data-stu-id="c720c-110">PARAMETERS</span></span>

### <span data-ttu-id="c720c-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="c720c-111">-Capacity</span></span>
<span data-ttu-id="c720c-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c720c-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="c720c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c720c-113">-DefaultProfile</span></span>
<span data-ttu-id="c720c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c720c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c720c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c720c-115">-Name</span></span>
<span data-ttu-id="c720c-116">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="c720c-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="c720c-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c720c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c720c-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="c720c-118">Standard_Small</span></span>
- <span data-ttu-id="c720c-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="c720c-119">Standard_Medium</span></span>
- <span data-ttu-id="c720c-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="c720c-120">Standard_Large</span></span>
- <span data-ttu-id="c720c-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="c720c-121">WAF_Medium</span></span>
- <span data-ttu-id="c720c-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="c720c-122">WAF_Large</span></span>

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

### <span data-ttu-id="c720c-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="c720c-123">-Tier</span></span>
<span data-ttu-id="c720c-124">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="c720c-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="c720c-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c720c-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c720c-126">Oficial</span><span class="sxs-lookup"><span data-stu-id="c720c-126">Standard</span></span>
- <span data-ttu-id="c720c-127">WAF</span><span class="sxs-lookup"><span data-stu-id="c720c-127">WAF</span></span>

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

### <span data-ttu-id="c720c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c720c-128">CommonParameters</span></span>
<span data-ttu-id="c720c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c720c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c720c-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c720c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c720c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c720c-131">INPUTS</span></span>

### <span data-ttu-id="c720c-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c720c-132">None</span></span>

## <span data-ttu-id="c720c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c720c-133">OUTPUTS</span></span>

### <span data-ttu-id="c720c-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c720c-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="c720c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c720c-135">NOTES</span></span>

## <span data-ttu-id="c720c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c720c-136">RELATED LINKS</span></span>

[<span data-ttu-id="c720c-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c720c-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="c720c-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="c720c-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


