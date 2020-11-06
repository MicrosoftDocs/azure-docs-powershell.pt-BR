---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439910"
---
# <span data-ttu-id="7db24-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7db24-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="7db24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7db24-102">SYNOPSIS</span></span>
<span data-ttu-id="7db24-103">Cria uma SKU para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7db24-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7db24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7db24-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7db24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7db24-105">DESCRIPTION</span></span>
<span data-ttu-id="7db24-106">O cmdlet **New-AzureRmApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7db24-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="7db24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7db24-107">EXAMPLES</span></span>

### <span data-ttu-id="7db24-108">Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="7db24-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="7db24-109">Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.</span><span class="sxs-lookup"><span data-stu-id="7db24-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="7db24-110">OS</span><span class="sxs-lookup"><span data-stu-id="7db24-110">PARAMETERS</span></span>

### <span data-ttu-id="7db24-111">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="7db24-111">-Capacity</span></span>
<span data-ttu-id="7db24-112">Especifica o número de instâncias de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7db24-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="7db24-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7db24-113">-Name</span></span>
<span data-ttu-id="7db24-114">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="7db24-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="7db24-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7db24-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7db24-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="7db24-116">Standard_Small</span></span>
- <span data-ttu-id="7db24-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="7db24-117">Standard_Medium</span></span>
- <span data-ttu-id="7db24-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="7db24-118">Standard_Large</span></span>
- <span data-ttu-id="7db24-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="7db24-119">WAF_Medium</span></span>
- <span data-ttu-id="7db24-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="7db24-120">WAF_Large</span></span>

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

### <span data-ttu-id="7db24-121">-Tier</span><span class="sxs-lookup"><span data-stu-id="7db24-121">-Tier</span></span>
<span data-ttu-id="7db24-122">Especifica o nível da SKU.</span><span class="sxs-lookup"><span data-stu-id="7db24-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="7db24-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7db24-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7db24-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="7db24-124">Standard</span></span>
- <span data-ttu-id="7db24-125">WAF</span><span class="sxs-lookup"><span data-stu-id="7db24-125">WAF</span></span>

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

### <span data-ttu-id="7db24-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db24-126">-DefaultProfile</span></span>
<span data-ttu-id="7db24-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7db24-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7db24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db24-128">CommonParameters</span></span>
<span data-ttu-id="7db24-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db24-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db24-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db24-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7db24-131">INPUTS</span></span>

### <span data-ttu-id="7db24-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7db24-132">System.String</span></span>

## <span data-ttu-id="7db24-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7db24-133">OUTPUTS</span></span>

### <span data-ttu-id="7db24-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7db24-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="7db24-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7db24-135">NOTES</span></span>

## <span data-ttu-id="7db24-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7db24-136">RELATED LINKS</span></span>

[<span data-ttu-id="7db24-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7db24-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="7db24-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="7db24-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


