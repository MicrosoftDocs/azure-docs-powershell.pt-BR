---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785489"
---
# <span data-ttu-id="f61dd-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f61dd-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="f61dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f61dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f61dd-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f61dd-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f61dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f61dd-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f61dd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f61dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f61dd-106">O cmdlet **New-AzureRmApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f61dd-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="f61dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f61dd-107">EXAMPLES</span></span>

### <span data-ttu-id="f61dd-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="f61dd-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="f61dd-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="f61dd-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="f61dd-110">OS</span><span class="sxs-lookup"><span data-stu-id="f61dd-110">PARAMETERS</span></span>

### <span data-ttu-id="f61dd-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="f61dd-111">-Capacity</span></span>
<span data-ttu-id="f61dd-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f61dd-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61dd-113">-DefaultProfile</span></span>
<span data-ttu-id="f61dd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f61dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f61dd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f61dd-115">-Name</span></span>
<span data-ttu-id="f61dd-116">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="f61dd-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="f61dd-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f61dd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f61dd-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="f61dd-118">Standard_Small</span></span>
- <span data-ttu-id="f61dd-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="f61dd-119">Standard_Medium</span></span>
- <span data-ttu-id="f61dd-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="f61dd-120">Standard_Large</span></span>
- <span data-ttu-id="f61dd-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="f61dd-121">WAF_Medium</span></span>
- <span data-ttu-id="f61dd-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="f61dd-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61dd-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="f61dd-123">-Tier</span></span>
<span data-ttu-id="f61dd-124">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="f61dd-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="f61dd-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f61dd-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f61dd-126">Oficial</span><span class="sxs-lookup"><span data-stu-id="f61dd-126">Standard</span></span>
- <span data-ttu-id="f61dd-127">WAF</span><span class="sxs-lookup"><span data-stu-id="f61dd-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f61dd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61dd-128">CommonParameters</span></span>
<span data-ttu-id="f61dd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f61dd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61dd-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f61dd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61dd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f61dd-131">INPUTS</span></span>

### <span data-ttu-id="f61dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f61dd-132">System.String</span></span>

## <span data-ttu-id="f61dd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f61dd-133">OUTPUTS</span></span>

### <span data-ttu-id="f61dd-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f61dd-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="f61dd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f61dd-135">NOTES</span></span>

## <span data-ttu-id="f61dd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f61dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="f61dd-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f61dd-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="f61dd-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f61dd-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


