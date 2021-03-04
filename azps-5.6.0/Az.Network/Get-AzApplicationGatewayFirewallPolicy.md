---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 122e011336b9fcdb8b8eb19622632e1ff295a01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891173"
---
# <span data-ttu-id="6ff84-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6ff84-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="6ff84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff84-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff84-103">Obtém uma política de firewall de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ff84-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="6ff84-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6ff84-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff84-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6ff84-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff84-106">O cmdlet **Get-AzApplicationGatewayFirewallPolicy** obtém uma política de firewall de gateway de aplicativo..</span><span class="sxs-lookup"><span data-stu-id="6ff84-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="6ff84-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ff84-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff84-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ff84-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6ff84-109">Esse comando obtém a política de firewall do gateway de aplicativo chamada FirewallPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="6ff84-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="6ff84-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6ff84-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff84-111">-DefaultProfile</span></span>
<span data-ttu-id="6ff84-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff84-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff84-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6ff84-113">-Name</span></span>
<span data-ttu-id="6ff84-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6ff84-114">The resource name.</span></span>

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

### <span data-ttu-id="6ff84-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff84-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ff84-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ff84-116">The resource group name.</span></span>

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

### <span data-ttu-id="6ff84-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff84-117">CommonParameters</span></span>
<span data-ttu-id="6ff84-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff84-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff84-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ff84-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff84-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ff84-120">INPUTS</span></span>

### <span data-ttu-id="6ff84-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6ff84-121">System.String</span></span>

## <span data-ttu-id="6ff84-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6ff84-122">OUTPUTS</span></span>

### <span data-ttu-id="6ff84-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6ff84-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="6ff84-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="6ff84-124">NOTES</span></span>

## <span data-ttu-id="6ff84-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ff84-125">RELATED LINKS</span></span>
