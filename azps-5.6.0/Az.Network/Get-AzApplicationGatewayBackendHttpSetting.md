---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 957417d7751080a82ddc8785abdd124c8f723303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892103"
---
# <span data-ttu-id="23f9d-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="23f9d-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="23f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="23f9d-103">Obtém as configurações HTTP back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23f9d-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="23f9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="23f9d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f9d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="23f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="23f9d-106">O Get-AzApplicationGatewayBackendHttpSetting cmdlet obtém as configurações HTTP back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23f9d-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="23f9d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="23f9d-108">Exemplo 1: Obter configurações HTTP back-end pelo nome</span><span class="sxs-lookup"><span data-stu-id="23f9d-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="23f9d-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém as configurações HTTP denominadas Configurações01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="23f9d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="23f9d-110">Exemplo 2: Obter uma coleção de configurações HTTP back-end</span><span class="sxs-lookup"><span data-stu-id="23f9d-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="23f9d-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a coleção de configurações HTTP para $AppGw e armazena as configurações na variável $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="23f9d-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="23f9d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="23f9d-112">PARAMETERS</span></span>

### <span data-ttu-id="23f9d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23f9d-113">-ApplicationGateway</span></span>
<span data-ttu-id="23f9d-114">Especifica um objeto gateway de aplicativo que contém configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="23f9d-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="23f9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f9d-115">-DefaultProfile</span></span>
<span data-ttu-id="23f9d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="23f9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23f9d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="23f9d-117">-Name</span></span>
<span data-ttu-id="23f9d-118">Especifica o nome das configurações HTTP de back-end que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="23f9d-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f9d-119">CommonParameters</span></span>
<span data-ttu-id="23f9d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f9d-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23f9d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f9d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23f9d-122">INPUTS</span></span>

### <span data-ttu-id="23f9d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23f9d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23f9d-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="23f9d-124">OUTPUTS</span></span>

### <span data-ttu-id="23f9d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="23f9d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="23f9d-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="23f9d-126">NOTES</span></span>

## <span data-ttu-id="23f9d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23f9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="23f9d-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="23f9d-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="23f9d-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="23f9d-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="23f9d-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="23f9d-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="23f9d-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="23f9d-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

