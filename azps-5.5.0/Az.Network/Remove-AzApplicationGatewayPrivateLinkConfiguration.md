---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115096"
---
# <span data-ttu-id="b9c1a-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c1a-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="b9c1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c1a-103">Remove uma configuração de privateLink de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="b9c1a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9c1a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c1a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9c1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c1a-106">O cmdlet **Remove-AzApplicationGatewayPrivateLinkConfiguration** remove uma configuração de privateLink de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="b9c1a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9c1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c1a-108">Exemplo 1: Remover uma configuração do gateway de aplicativo PrivateLink</span><span class="sxs-lookup"><span data-stu-id="b9c1a-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="b9c1a-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9c1a-110">O segundo comando remove a configuração privateLink chamada privateLinkConfig01 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b9c1a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9c1a-111">PARAMETERS</span></span>

### <span data-ttu-id="b9c1a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c1a-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9c1a-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c1a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b9c1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c1a-114">-DefaultProfile</span></span>
<span data-ttu-id="b9c1a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c1a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c1a-116">-Name</span></span>
<span data-ttu-id="b9c1a-117">O nome da configuração do gateway de aplicativo privateLink</span><span class="sxs-lookup"><span data-stu-id="b9c1a-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="b9c1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c1a-118">CommonParameters</span></span>
<span data-ttu-id="b9c1a-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c1a-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9c1a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c1a-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9c1a-121">INPUTS</span></span>

### <span data-ttu-id="b9c1a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c1a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9c1a-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9c1a-123">OUTPUTS</span></span>

### <span data-ttu-id="b9c1a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c1a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9c1a-125">Notas</span><span class="sxs-lookup"><span data-stu-id="b9c1a-125">NOTES</span></span>

## <span data-ttu-id="b9c1a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9c1a-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c1a-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9c1a-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c1a-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9c1a-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c1a-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9c1a-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c1a-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)