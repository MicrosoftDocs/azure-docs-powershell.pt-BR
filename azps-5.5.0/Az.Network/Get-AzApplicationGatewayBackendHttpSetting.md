---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114180"
---
# <span data-ttu-id="493fe-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="493fe-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="493fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="493fe-102">SYNOPSIS</span></span>
<span data-ttu-id="493fe-103">Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="493fe-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="493fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="493fe-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493fe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="493fe-105">DESCRIPTION</span></span>
<span data-ttu-id="493fe-106">O Get-AzApplicationGatewayBackendHttpSetting cmdlet obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="493fe-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="493fe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="493fe-107">EXAMPLES</span></span>

### <span data-ttu-id="493fe-108">Exemplo 1: Obter configurações HTTP de back-end por nome</span><span class="sxs-lookup"><span data-stu-id="493fe-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="493fe-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw usuário. O segundo comando obtém as configurações HTTP chamadas Configurações01 para $AppGw e armazena as configurações na variável $Settings dados.</span><span class="sxs-lookup"><span data-stu-id="493fe-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="493fe-110">Exemplo 2: Obter um conjunto de configurações HTTP de back-end</span><span class="sxs-lookup"><span data-stu-id="493fe-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="493fe-111">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw usuário. O segundo comando obtém o conjunto de configurações HTTP para $AppGw e armazena as configurações na variável $SettingsList dados.</span><span class="sxs-lookup"><span data-stu-id="493fe-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="493fe-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="493fe-112">PARAMETERS</span></span>

### <span data-ttu-id="493fe-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="493fe-113">-ApplicationGateway</span></span>
<span data-ttu-id="493fe-114">Especifica um objeto de gateway de aplicativo que contém configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="493fe-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="493fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493fe-115">-DefaultProfile</span></span>
<span data-ttu-id="493fe-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="493fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="493fe-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="493fe-117">-Name</span></span>
<span data-ttu-id="493fe-118">Especifica o nome das configurações HTTP de back-end que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="493fe-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="493fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493fe-119">CommonParameters</span></span>
<span data-ttu-id="493fe-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="493fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493fe-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="493fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493fe-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="493fe-122">INPUTS</span></span>

### <span data-ttu-id="493fe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="493fe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="493fe-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="493fe-124">OUTPUTS</span></span>

### <span data-ttu-id="493fe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="493fe-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="493fe-126">Notas</span><span class="sxs-lookup"><span data-stu-id="493fe-126">NOTES</span></span>

## <span data-ttu-id="493fe-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="493fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="493fe-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="493fe-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="493fe-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="493fe-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="493fe-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="493fe-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="493fe-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="493fe-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

