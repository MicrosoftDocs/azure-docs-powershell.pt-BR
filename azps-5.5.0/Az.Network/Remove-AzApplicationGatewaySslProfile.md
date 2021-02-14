---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117353"
---
# <span data-ttu-id="2c7ac-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2c7ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7ac-103">Remove o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="2c7ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c7ac-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c7ac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c7ac-105">DESCRIPTION</span></span>
<span data-ttu-id="2c7ac-106">O cmdlet **Remove-AzApplicationGatewaySslProfile** remove o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="2c7ac-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c7ac-107">EXAMPLES</span></span>

### <span data-ttu-id="2c7ac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c7ac-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="2c7ac-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2c7ac-110">O segundo comando remove o perfil SSL chamado SslProfile01 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2c7ac-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c7ac-111">PARAMETERS</span></span>

### <span data-ttu-id="2c7ac-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c7ac-112">-ApplicationGateway</span></span>
<span data-ttu-id="2c7ac-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c7ac-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2c7ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-114">-DefaultProfile</span></span>
<span data-ttu-id="2c7ac-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c7ac-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c7ac-116">-Name</span></span>
<span data-ttu-id="2c7ac-117">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="2c7ac-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="2c7ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7ac-118">CommonParameters</span></span>
<span data-ttu-id="2c7ac-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7ac-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c7ac-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7ac-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c7ac-121">INPUTS</span></span>

### <span data-ttu-id="2c7ac-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c7ac-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c7ac-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c7ac-123">OUTPUTS</span></span>

### <span data-ttu-id="2c7ac-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c7ac-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c7ac-125">Notas</span><span class="sxs-lookup"><span data-stu-id="2c7ac-125">NOTES</span></span>

## <span data-ttu-id="2c7ac-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c7ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="2c7ac-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c7ac-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c7ac-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="2c7ac-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c7ac-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)