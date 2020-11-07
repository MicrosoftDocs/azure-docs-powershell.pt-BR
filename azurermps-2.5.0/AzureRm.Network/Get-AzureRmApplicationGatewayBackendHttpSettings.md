---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 366b3545e54c1465bf2eaf050a9e9199288fce5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785728"
---
# <span data-ttu-id="7b8fc-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7b8fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8fc-103">Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b8fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b8fc-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b8fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8fc-106">O cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings Obtém as configurações HTTP de back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7b8fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b8fc-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8fc-108">Exemplo 1: obter configurações HTTP back-end por nome</span><span class="sxs-lookup"><span data-stu-id="7b8fc-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7b8fc-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém as configurações de HTTP chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="7b8fc-110">Exemplo 2: obter uma coleção de configurações HTTP back-end</span><span class="sxs-lookup"><span data-stu-id="7b8fc-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="7b8fc-111">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém a coleção de configurações HTTP para $AppGw e armazena as configurações na variável $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="7b8fc-112">OS</span><span class="sxs-lookup"><span data-stu-id="7b8fc-112">PARAMETERS</span></span>

### <span data-ttu-id="7b8fc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b8fc-113">-ApplicationGateway</span></span>
<span data-ttu-id="7b8fc-114">Especifica um objeto do aplicativo gateway que contém as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7b8fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8fc-115">-DefaultProfile</span></span>
<span data-ttu-id="7b8fc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8fc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b8fc-117">-Name</span></span>
<span data-ttu-id="7b8fc-118">Especifica o nome das configurações HTTP de back-end que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7b8fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8fc-119">CommonParameters</span></span>
<span data-ttu-id="7b8fc-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8fc-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8fc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8fc-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b8fc-122">INPUTS</span></span>

### <span data-ttu-id="7b8fc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7b8fc-123">System.String</span></span>

## <span data-ttu-id="7b8fc-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b8fc-124">OUTPUTS</span></span>

### <span data-ttu-id="7b8fc-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7b8fc-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b8fc-126">NOTES</span></span>

## <span data-ttu-id="7b8fc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b8fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b8fc-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7b8fc-129">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7b8fc-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7b8fc-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7b8fc-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

