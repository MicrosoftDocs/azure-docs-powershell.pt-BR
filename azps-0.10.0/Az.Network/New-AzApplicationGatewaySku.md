---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775421"
---
# <span data-ttu-id="619f6-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="619f6-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="619f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="619f6-102">SYNOPSIS</span></span>
<span data-ttu-id="619f6-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="619f6-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="619f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="619f6-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="619f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="619f6-105">DESCRIPTION</span></span>
<span data-ttu-id="619f6-106">O cmdlet **New-AzApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="619f6-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="619f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="619f6-107">EXAMPLES</span></span>

### <span data-ttu-id="619f6-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="619f6-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="619f6-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="619f6-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="619f6-110">OS</span><span class="sxs-lookup"><span data-stu-id="619f6-110">PARAMETERS</span></span>

### <span data-ttu-id="619f6-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="619f6-111">-Capacity</span></span>
<span data-ttu-id="619f6-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="619f6-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="619f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619f6-113">-DefaultProfile</span></span>
<span data-ttu-id="619f6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="619f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="619f6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="619f6-115">-Name</span></span>
<span data-ttu-id="619f6-116">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="619f6-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="619f6-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="619f6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="619f6-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="619f6-118">Standard_Small</span></span>
- <span data-ttu-id="619f6-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="619f6-119">Standard_Medium</span></span>
- <span data-ttu-id="619f6-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="619f6-120">Standard_Large</span></span>
- <span data-ttu-id="619f6-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="619f6-121">WAF_Medium</span></span>
- <span data-ttu-id="619f6-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="619f6-122">WAF_Large</span></span>

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

### <span data-ttu-id="619f6-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="619f6-123">-Tier</span></span>
<span data-ttu-id="619f6-124">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="619f6-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="619f6-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="619f6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="619f6-126">Oficial</span><span class="sxs-lookup"><span data-stu-id="619f6-126">Standard</span></span>
- <span data-ttu-id="619f6-127">WAF</span><span class="sxs-lookup"><span data-stu-id="619f6-127">WAF</span></span>

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

### <span data-ttu-id="619f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619f6-128">CommonParameters</span></span>
<span data-ttu-id="619f6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619f6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="619f6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619f6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="619f6-131">INPUTS</span></span>

### <span data-ttu-id="619f6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="619f6-132">System.String</span></span>

## <span data-ttu-id="619f6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="619f6-133">OUTPUTS</span></span>

### <span data-ttu-id="619f6-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="619f6-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="619f6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="619f6-135">NOTES</span></span>

## <span data-ttu-id="619f6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="619f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="619f6-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="619f6-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="619f6-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="619f6-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


