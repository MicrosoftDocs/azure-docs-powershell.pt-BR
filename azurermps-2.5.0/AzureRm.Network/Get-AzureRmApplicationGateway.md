---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 2b6373944f8b7bbc741557629fad7c9f717e979e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786488"
---
# <span data-ttu-id="190bc-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="190bc-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="190bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="190bc-102">SYNOPSIS</span></span>
<span data-ttu-id="190bc-103">Obtém um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="190bc-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="190bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="190bc-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="190bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="190bc-105">DESCRIPTION</span></span>
<span data-ttu-id="190bc-106">O cmdlet **Get-AzureRmApplicationGateway** Obtém um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="190bc-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="190bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="190bc-107">EXAMPLES</span></span>

### <span data-ttu-id="190bc-108">Exemplo 1: obter um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="190bc-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="190bc-109">Esse comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="190bc-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="190bc-110">Exemplo 2: obter uma lista dos gateways do aplicativo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="190bc-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="190bc-111">Esse comando obtém uma lista de todos os gateways do aplicativo no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="190bc-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="190bc-112">Exemplo 3: obter uma lista dos gateways do aplicativo em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="190bc-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="190bc-113">Esse comando obtém uma lista de todos os gateways de aplicativo na assinatura e armazena-o na variável $AppGwList.</span><span class="sxs-lookup"><span data-stu-id="190bc-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="190bc-114">OS</span><span class="sxs-lookup"><span data-stu-id="190bc-114">PARAMETERS</span></span>

### <span data-ttu-id="190bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190bc-115">-DefaultProfile</span></span>
<span data-ttu-id="190bc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="190bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="190bc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="190bc-117">-Name</span></span>
<span data-ttu-id="190bc-118">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="190bc-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="190bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="190bc-120">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="190bc-120">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="190bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190bc-121">CommonParameters</span></span>
<span data-ttu-id="190bc-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190bc-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190bc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190bc-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="190bc-124">INPUTS</span></span>

### <span data-ttu-id="190bc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="190bc-125">System.String</span></span>

## <span data-ttu-id="190bc-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="190bc-126">OUTPUTS</span></span>

### <span data-ttu-id="190bc-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="190bc-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="190bc-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="190bc-128">NOTES</span></span>

## <span data-ttu-id="190bc-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="190bc-129">RELATED LINKS</span></span>

[<span data-ttu-id="190bc-130">Parar-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="190bc-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


