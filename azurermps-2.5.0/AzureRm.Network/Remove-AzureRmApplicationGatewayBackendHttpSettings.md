---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785663"
---
# <span data-ttu-id="210b4-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210b4-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="210b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="210b4-102">SYNOPSIS</span></span>
<span data-ttu-id="210b4-103">Remove as configurações HTTP de back-end de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="210b4-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="210b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="210b4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="210b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="210b4-105">DESCRIPTION</span></span>
<span data-ttu-id="210b4-106">O cmdlet Remove-AzureRmApplicationGatewayBackendHttpSettings remove as configurações de protocolo de transferência de hipertexto (HTTP) back-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="210b4-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="210b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="210b4-107">EXAMPLES</span></span>

### <span data-ttu-id="210b4-108">Exemplo 1: remover as configurações HTTP de back-end de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="210b4-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="210b4-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="210b4-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="210b4-110">O segundo comando Remove a configuração HTTP back-end chamada BackEndSetting02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="210b4-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="210b4-111">OS</span><span class="sxs-lookup"><span data-stu-id="210b4-111">PARAMETERS</span></span>

### <span data-ttu-id="210b4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="210b4-112">-ApplicationGateway</span></span>
<span data-ttu-id="210b4-113">Especifica o Application Gateway do qual esse cmdlet Remove as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="210b4-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="210b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210b4-114">-DefaultProfile</span></span>
<span data-ttu-id="210b4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="210b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="210b4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="210b4-116">-Name</span></span>
<span data-ttu-id="210b4-117">Especifica o nome das configurações HTTP de back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="210b4-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="210b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210b4-118">CommonParameters</span></span>
<span data-ttu-id="210b4-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210b4-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="210b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210b4-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="210b4-121">INPUTS</span></span>

### <span data-ttu-id="210b4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="210b4-122">System.String</span></span>

## <span data-ttu-id="210b4-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="210b4-123">OUTPUTS</span></span>

### <span data-ttu-id="210b4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="210b4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="210b4-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="210b4-125">NOTES</span></span>

## <span data-ttu-id="210b4-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="210b4-126">RELATED LINKS</span></span>

[<span data-ttu-id="210b4-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210b4-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="210b4-128">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210b4-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="210b4-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210b4-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="210b4-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210b4-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

