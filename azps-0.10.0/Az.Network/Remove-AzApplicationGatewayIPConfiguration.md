---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 68fa8e24d9cdc5e5dbf04ed132e1eac4909973d4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775329"
---
# <span data-ttu-id="f5742-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5742-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="f5742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5742-102">SYNOPSIS</span></span>
<span data-ttu-id="f5742-103">Remove uma configuração de IP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="f5742-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="f5742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5742-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5742-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5742-105">DESCRIPTION</span></span>
<span data-ttu-id="f5742-106">O cmdlet **Remove-AzApplicationGatewayIPConfiguration** remove uma configuração de IP de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5742-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="f5742-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5742-107">EXAMPLES</span></span>

### <span data-ttu-id="f5742-108">Exemplo 1: remover uma configuração de IP de um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="f5742-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="f5742-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f5742-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f5742-110">O segundo comando Remove a configuração de IP denominada Subnet02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f5742-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f5742-111">OS</span><span class="sxs-lookup"><span data-stu-id="f5742-111">PARAMETERS</span></span>

### <span data-ttu-id="f5742-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5742-112">-ApplicationGateway</span></span>
<span data-ttu-id="f5742-113">Especifica o gateway do aplicativo do qual remover uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="f5742-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5742-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5742-114">-DefaultProfile</span></span>
<span data-ttu-id="f5742-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5742-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5742-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5742-116">-Name</span></span>
<span data-ttu-id="f5742-117">Especifica o nome da configuração de IP a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f5742-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5742-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5742-118">CommonParameters</span></span>
<span data-ttu-id="f5742-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5742-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5742-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5742-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5742-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5742-121">INPUTS</span></span>

### <span data-ttu-id="f5742-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f5742-122">System.String</span></span>

## <span data-ttu-id="f5742-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5742-123">OUTPUTS</span></span>

### <span data-ttu-id="f5742-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5742-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5742-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5742-125">NOTES</span></span>

## <span data-ttu-id="f5742-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5742-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5742-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5742-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5742-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5742-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5742-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5742-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f5742-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5742-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

