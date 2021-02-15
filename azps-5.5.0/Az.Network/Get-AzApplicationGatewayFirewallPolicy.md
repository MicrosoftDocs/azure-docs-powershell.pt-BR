---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111700"
---
# <span data-ttu-id="8999d-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8999d-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="8999d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8999d-102">SYNOPSIS</span></span>
<span data-ttu-id="8999d-103">Obtém uma política de firewall do gateway de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8999d-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="8999d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8999d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8999d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8999d-105">DESCRIPTION</span></span>
<span data-ttu-id="8999d-106">O cmdlet **Get-AzApplicationGatewayFirewallPolicy** obtém uma política de firewall do gateway de aplicativos..</span><span class="sxs-lookup"><span data-stu-id="8999d-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="8999d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8999d-107">EXAMPLES</span></span>

### <span data-ttu-id="8999d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8999d-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8999d-109">Esse comando obtém a política de firewall do gateway de aplicativo chamada FirewallPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="8999d-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="8999d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8999d-110">PARAMETERS</span></span>

### <span data-ttu-id="8999d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8999d-111">-DefaultProfile</span></span>
<span data-ttu-id="8999d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8999d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8999d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8999d-113">-Name</span></span>
<span data-ttu-id="8999d-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8999d-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8999d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8999d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8999d-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8999d-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8999d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8999d-117">CommonParameters</span></span>
<span data-ttu-id="8999d-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8999d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8999d-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8999d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8999d-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="8999d-120">INPUTS</span></span>

### <span data-ttu-id="8999d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8999d-121">System.String</span></span>

## <span data-ttu-id="8999d-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="8999d-122">OUTPUTS</span></span>

### <span data-ttu-id="8999d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8999d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="8999d-124">Notas</span><span class="sxs-lookup"><span data-stu-id="8999d-124">NOTES</span></span>

## <span data-ttu-id="8999d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8999d-125">RELATED LINKS</span></span>
