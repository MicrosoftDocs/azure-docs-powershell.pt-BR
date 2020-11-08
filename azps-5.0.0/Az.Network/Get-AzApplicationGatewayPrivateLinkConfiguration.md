---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125937"
---
# <span data-ttu-id="872ed-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="872ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="872ed-102">SYNOPSIS</span></span>
<span data-ttu-id="872ed-103">Obtém a configuração do vínculo particular de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="872ed-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="872ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="872ed-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="872ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="872ed-105">DESCRIPTION</span></span>
<span data-ttu-id="872ed-106">O cmdlet **Get-AzApplicationGatewayPrivateLinkConfiguration** Obtém a configuração do link privado de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="872ed-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="872ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="872ed-107">EXAMPLES</span></span>

### <span data-ttu-id="872ed-108">Exemplo 1: obter uma configuração de link particular especificado</span><span class="sxs-lookup"><span data-stu-id="872ed-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="872ed-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="872ed-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="872ed-110">O segundo comando obtém a configuração do link particular chamado privateLinkConfig01 do $AppGw e a armazena na variável $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="872ed-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="872ed-111">Exemplo 2: obter uma lista de configurações de link particular</span><span class="sxs-lookup"><span data-stu-id="872ed-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="872ed-112">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="872ed-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="872ed-113">O segundo comando obtém todas as configurações de vínculo privado $AppGw e as armazena na variável $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="872ed-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="872ed-114">OS</span><span class="sxs-lookup"><span data-stu-id="872ed-114">PARAMETERS</span></span>

### <span data-ttu-id="872ed-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="872ed-115">-ApplicationGateway</span></span>
<span data-ttu-id="872ed-116">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="872ed-116">The applicationGateway</span></span>

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

### <span data-ttu-id="872ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872ed-117">-DefaultProfile</span></span>
<span data-ttu-id="872ed-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="872ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="872ed-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="872ed-119">-Name</span></span>
<span data-ttu-id="872ed-120">O nome da configuração de privateLink do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="872ed-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="872ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872ed-121">CommonParameters</span></span>
<span data-ttu-id="872ed-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872ed-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="872ed-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872ed-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="872ed-124">INPUTS</span></span>

### <span data-ttu-id="872ed-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="872ed-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="872ed-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="872ed-126">OUTPUTS</span></span>

### <span data-ttu-id="872ed-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="872ed-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="872ed-128">NOTES</span></span>

## <span data-ttu-id="872ed-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="872ed-129">RELATED LINKS</span></span>

[<span data-ttu-id="872ed-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="872ed-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="872ed-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="872ed-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="872ed-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)