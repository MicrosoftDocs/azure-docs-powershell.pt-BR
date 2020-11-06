---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 2c49a71521e40cbe9e42c1a06c5c3d785a74d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602736"
---
# <span data-ttu-id="63e72-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63e72-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="63e72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63e72-102">SYNOPSIS</span></span>
<span data-ttu-id="63e72-103">Obtém um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63e72-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63e72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63e72-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63e72-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63e72-105">DESCRIPTION</span></span>
<span data-ttu-id="63e72-106">O cmdlet **Get-AzureRmApplicationGateway** Obtém um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="63e72-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="63e72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63e72-107">EXAMPLES</span></span>

### <span data-ttu-id="63e72-108">Exemplo 1: obter um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="63e72-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63e72-109">Esse comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="63e72-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="63e72-110">Exemplo 2: obter uma lista dos gateways do aplicativo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="63e72-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63e72-111">Esse comando obtém uma lista de todos os gateways do aplicativo no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="63e72-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="63e72-112">Exemplo 3: obter uma lista dos gateways do aplicativo em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="63e72-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="63e72-113">Esse comando obtém uma lista de todos os gateways de aplicativo na assinatura e armazena-o na variável $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="63e72-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="63e72-114">OS</span><span class="sxs-lookup"><span data-stu-id="63e72-114">PARAMETERS</span></span>

### <span data-ttu-id="63e72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e72-115">-DefaultProfile</span></span>
<span data-ttu-id="63e72-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63e72-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e72-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="63e72-117">-Name</span></span>
<span data-ttu-id="63e72-118">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="63e72-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e72-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e72-119">-ResourceGroupName</span></span>
<span data-ttu-id="63e72-120">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="63e72-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63e72-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e72-121">CommonParameters</span></span>
<span data-ttu-id="63e72-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e72-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e72-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63e72-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e72-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63e72-124">INPUTS</span></span>

### <span data-ttu-id="63e72-125">System. String</span><span class="sxs-lookup"><span data-stu-id="63e72-125">System.String</span></span>

## <span data-ttu-id="63e72-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63e72-126">OUTPUTS</span></span>

### <span data-ttu-id="63e72-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63e72-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63e72-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63e72-128">NOTES</span></span>

## <span data-ttu-id="63e72-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e72-129">RELATED LINKS</span></span>

[<span data-ttu-id="63e72-130">Parar-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63e72-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


