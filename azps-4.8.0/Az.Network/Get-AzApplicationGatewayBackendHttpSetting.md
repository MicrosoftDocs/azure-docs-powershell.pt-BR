---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955440"
---
# <span data-ttu-id="787a8-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="787a8-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="787a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="787a8-102">SYNOPSIS</span></span>
<span data-ttu-id="787a8-103">Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="787a8-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="787a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="787a8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="787a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="787a8-105">DESCRIPTION</span></span>
<span data-ttu-id="787a8-106">O cmdlet Get-AzApplicationGatewayBackendHttpSetting Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="787a8-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="787a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="787a8-107">EXAMPLES</span></span>

### <span data-ttu-id="787a8-108">Exemplo 1: obter configurações HTTP back-end por nome</span><span class="sxs-lookup"><span data-stu-id="787a8-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="787a8-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém as configurações de HTTP chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="787a8-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="787a8-110">Exemplo 2: obter uma coleção de configurações HTTP back-end</span><span class="sxs-lookup"><span data-stu-id="787a8-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="787a8-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a coleção de configurações HTTP para $AppGw e armazena as configurações na variável $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="787a8-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="787a8-112">OS</span><span class="sxs-lookup"><span data-stu-id="787a8-112">PARAMETERS</span></span>

### <span data-ttu-id="787a8-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="787a8-113">-ApplicationGateway</span></span>
<span data-ttu-id="787a8-114">Especifica um objeto do aplicativo gateway que contém as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="787a8-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="787a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787a8-115">-DefaultProfile</span></span>
<span data-ttu-id="787a8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="787a8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="787a8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="787a8-117">-Name</span></span>
<span data-ttu-id="787a8-118">Especifica o nome das configurações HTTP de back-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="787a8-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="787a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787a8-119">CommonParameters</span></span>
<span data-ttu-id="787a8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787a8-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787a8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787a8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="787a8-122">INPUTS</span></span>

### <span data-ttu-id="787a8-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="787a8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="787a8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="787a8-124">OUTPUTS</span></span>

### <span data-ttu-id="787a8-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="787a8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="787a8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="787a8-126">NOTES</span></span>

## <span data-ttu-id="787a8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="787a8-127">RELATED LINKS</span></span>

[<span data-ttu-id="787a8-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="787a8-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="787a8-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="787a8-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="787a8-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="787a8-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="787a8-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="787a8-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

