---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257160"
---
# <span data-ttu-id="5eca1-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5eca1-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="5eca1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5eca1-102">SYNOPSIS</span></span>
<span data-ttu-id="5eca1-103">Remove as configurações HTTP de back-end de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="5eca1-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="5eca1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5eca1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eca1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5eca1-105">DESCRIPTION</span></span>
<span data-ttu-id="5eca1-106">O cmdlet Remove-AzApplicationGatewayBackendHttpSetting remove as configurações de protocolo de transferência de hipertexto (HTTP) back-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eca1-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="5eca1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eca1-107">EXAMPLES</span></span>

### <span data-ttu-id="5eca1-108">Exemplo 1: remover as configurações HTTP de back-end de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="5eca1-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="5eca1-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5eca1-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5eca1-110">O segundo comando Remove a configuração HTTP back-end chamada BackEndSetting02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5eca1-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5eca1-111">OS</span><span class="sxs-lookup"><span data-stu-id="5eca1-111">PARAMETERS</span></span>

### <span data-ttu-id="5eca1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5eca1-112">-ApplicationGateway</span></span>
<span data-ttu-id="5eca1-113">Especifica o Application Gateway do qual esse cmdlet Remove as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="5eca1-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eca1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eca1-114">-DefaultProfile</span></span>
<span data-ttu-id="5eca1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5eca1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eca1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5eca1-116">-Name</span></span>
<span data-ttu-id="5eca1-117">Especifica o nome das configurações HTTP de back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5eca1-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eca1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eca1-118">CommonParameters</span></span>
<span data-ttu-id="5eca1-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eca1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eca1-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eca1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eca1-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5eca1-121">INPUTS</span></span>

### <span data-ttu-id="5eca1-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5eca1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5eca1-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5eca1-123">OUTPUTS</span></span>

### <span data-ttu-id="5eca1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5eca1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5eca1-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5eca1-125">NOTES</span></span>

## <span data-ttu-id="5eca1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eca1-126">RELATED LINKS</span></span>

[<span data-ttu-id="5eca1-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5eca1-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5eca1-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5eca1-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5eca1-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5eca1-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5eca1-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5eca1-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

