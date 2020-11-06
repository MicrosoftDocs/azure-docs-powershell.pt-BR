---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430986"
---
# <span data-ttu-id="7e689-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7e689-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e689-102">SYNOPSIS</span></span>
<span data-ttu-id="7e689-103">Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7e689-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e689-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e689-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e689-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e689-105">DESCRIPTION</span></span>
<span data-ttu-id="7e689-106">O cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7e689-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7e689-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e689-107">EXAMPLES</span></span>

### <span data-ttu-id="7e689-108">Exemplo 1: obter configurações HTTP back-end por nome</span><span class="sxs-lookup"><span data-stu-id="7e689-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7e689-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém as configurações de HTTP chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="7e689-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="7e689-110">Exemplo 2: obter uma coleção de configurações HTTP back-end</span><span class="sxs-lookup"><span data-stu-id="7e689-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="7e689-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a coleção de configurações HTTP para $AppGw e armazena as configurações na variável $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="7e689-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="7e689-112">OS</span><span class="sxs-lookup"><span data-stu-id="7e689-112">PARAMETERS</span></span>

### <span data-ttu-id="7e689-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e689-113">-ApplicationGateway</span></span>
<span data-ttu-id="7e689-114">Especifica um objeto do aplicativo gateway que contém as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="7e689-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7e689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e689-115">-DefaultProfile</span></span>
<span data-ttu-id="7e689-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e689-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e689-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e689-117">-Name</span></span>
<span data-ttu-id="7e689-118">Especifica o nome das configurações HTTP de back-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7e689-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e689-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e689-119">CommonParameters</span></span>
<span data-ttu-id="7e689-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e689-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e689-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e689-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e689-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e689-122">INPUTS</span></span>

### <span data-ttu-id="7e689-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7e689-123">System.String</span></span>

## <span data-ttu-id="7e689-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e689-124">OUTPUTS</span></span>

### <span data-ttu-id="7e689-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7e689-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e689-126">NOTES</span></span>

## <span data-ttu-id="7e689-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e689-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e689-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7e689-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7e689-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7e689-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7e689-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()
