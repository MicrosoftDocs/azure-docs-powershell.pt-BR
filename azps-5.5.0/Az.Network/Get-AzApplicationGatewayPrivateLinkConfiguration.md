---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117465"
---
# <span data-ttu-id="6f77a-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6f77a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f77a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f77a-103">Obtém a configuração de link privado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f77a-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="6f77a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f77a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f77a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f77a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f77a-106">O cmdlet **Get-AzApplicationGatewayPrivateLinkConfiguration** obtém a configuração de link particular de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f77a-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="6f77a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f77a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f77a-108">Exemplo 1: Obter uma configuração de link particular especificada</span><span class="sxs-lookup"><span data-stu-id="6f77a-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6f77a-109">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6f77a-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6f77a-110">O segundo comando obtém a configuração de link particular chamada privateLinkConfig01 do $AppGw e a armazena na variável $PrivateLinkConfiguration privada.</span><span class="sxs-lookup"><span data-stu-id="6f77a-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="6f77a-111">Exemplo 2: Obter uma lista de configuração de link particular</span><span class="sxs-lookup"><span data-stu-id="6f77a-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="6f77a-112">O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6f77a-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6f77a-113">O segundo comando obtém todas as configurações de link privado $AppGw e o armazena na variável $PrivateLinkConfigurations privada.</span><span class="sxs-lookup"><span data-stu-id="6f77a-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="6f77a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f77a-114">PARAMETERS</span></span>

### <span data-ttu-id="6f77a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f77a-115">-ApplicationGateway</span></span>
<span data-ttu-id="6f77a-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f77a-116">The applicationGateway</span></span>

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

### <span data-ttu-id="6f77a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f77a-117">-DefaultProfile</span></span>
<span data-ttu-id="6f77a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f77a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f77a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f77a-119">-Name</span></span>
<span data-ttu-id="6f77a-120">O nome da configuração do gateway de aplicativo privateLink</span><span class="sxs-lookup"><span data-stu-id="6f77a-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="6f77a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f77a-121">CommonParameters</span></span>
<span data-ttu-id="6f77a-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f77a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f77a-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f77a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f77a-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="6f77a-124">INPUTS</span></span>

### <span data-ttu-id="6f77a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f77a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f77a-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="6f77a-126">OUTPUTS</span></span>

### <span data-ttu-id="6f77a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="6f77a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="6f77a-128">NOTES</span></span>

## <span data-ttu-id="6f77a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f77a-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f77a-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6f77a-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6f77a-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="6f77a-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f77a-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)