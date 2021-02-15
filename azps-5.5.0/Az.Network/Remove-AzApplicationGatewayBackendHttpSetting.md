---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117365"
---
# <span data-ttu-id="67020-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67020-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="67020-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67020-102">SYNOPSIS</span></span>
<span data-ttu-id="67020-103">Remove as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67020-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="67020-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67020-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67020-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="67020-105">DESCRIPTION</span></span>
<span data-ttu-id="67020-106">O Remove-AzApplicationGatewayBackendHttpSetting cmdlet remove as configurações http de protocolo HTTP de back-end de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="67020-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="67020-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67020-107">EXAMPLES</span></span>

### <span data-ttu-id="67020-108">Exemplo 1: Remover configurações HTTP de back-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="67020-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="67020-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="67020-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="67020-110">O segundo comando remove a configuração HTTP de back-end chamada BackEndSetting02 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="67020-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="67020-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67020-111">PARAMETERS</span></span>

### <span data-ttu-id="67020-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67020-112">-ApplicationGateway</span></span>
<span data-ttu-id="67020-113">Especifica o gateway do aplicativo do qual este cmdlet remove as configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="67020-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="67020-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67020-114">-DefaultProfile</span></span>
<span data-ttu-id="67020-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="67020-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67020-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="67020-116">-Name</span></span>
<span data-ttu-id="67020-117">Especifica o nome das configurações HTTP de back-end que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="67020-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="67020-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67020-118">CommonParameters</span></span>
<span data-ttu-id="67020-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67020-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67020-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67020-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67020-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="67020-121">INPUTS</span></span>

### <span data-ttu-id="67020-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67020-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67020-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="67020-123">OUTPUTS</span></span>

### <span data-ttu-id="67020-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67020-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67020-125">Notas</span><span class="sxs-lookup"><span data-stu-id="67020-125">NOTES</span></span>

## <span data-ttu-id="67020-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67020-126">RELATED LINKS</span></span>

[<span data-ttu-id="67020-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67020-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="67020-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67020-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="67020-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67020-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="67020-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="67020-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

