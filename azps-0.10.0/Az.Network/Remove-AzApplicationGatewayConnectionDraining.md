---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 081b045550b9f8cb7ab3e4c6e59553c25bac567f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775332"
---
# <span data-ttu-id="d0314-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d0314-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d0314-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0314-102">SYNOPSIS</span></span>
<span data-ttu-id="d0314-103">Remove a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="d0314-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d0314-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0314-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0314-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0314-105">DESCRIPTION</span></span>
<span data-ttu-id="d0314-106">O cmdlet **Remove-AzApplicationGatewayConnectionDraining** remove a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="d0314-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="d0314-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0314-107">EXAMPLES</span></span>

### <span data-ttu-id="d0314-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0314-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="d0314-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d0314-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0314-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="d0314-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="d0314-111">O último comando Remove a conexão que descarrega a configuração das configurações HTTP de back-end armazenadas em $Settings.</span><span class="sxs-lookup"><span data-stu-id="d0314-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="d0314-112">OS</span><span class="sxs-lookup"><span data-stu-id="d0314-112">PARAMETERS</span></span>

### <span data-ttu-id="d0314-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0314-113">-BackendHttpSettings</span></span>
<span data-ttu-id="d0314-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="d0314-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0314-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0314-115">-DefaultProfile</span></span>
<span data-ttu-id="d0314-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0314-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0314-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0314-117">CommonParameters</span></span>
<span data-ttu-id="d0314-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0314-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0314-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0314-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0314-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0314-120">INPUTS</span></span>

### <span data-ttu-id="d0314-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0314-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d0314-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0314-122">OUTPUTS</span></span>

### <span data-ttu-id="d0314-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0314-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="d0314-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0314-124">NOTES</span></span>

## <span data-ttu-id="d0314-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0314-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0314-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0314-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d0314-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="d0314-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="d0314-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d0314-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d0314-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d0314-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d0314-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d0314-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
