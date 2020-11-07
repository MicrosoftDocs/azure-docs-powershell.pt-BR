---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 652583ff4425c0403440856a32be3b8107d771ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771806"
---
# <span data-ttu-id="ea7be-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7be-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="ea7be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea7be-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7be-103">Obtém uma política de firewall do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea7be-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="ea7be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea7be-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7be-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea7be-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7be-106">O cmdlet **Get-AzApplicationGatewayFirewallPolicy** Obtém uma política de firewall do Application Gateway..</span><span class="sxs-lookup"><span data-stu-id="ea7be-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="ea7be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea7be-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7be-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea7be-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ea7be-109">Esse comando obtém a política de firewall do gateway do aplicativo chamada FirewallPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ea7be-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="ea7be-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea7be-110">PARAMETERS</span></span>

### <span data-ttu-id="ea7be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7be-111">-DefaultProfile</span></span>
<span data-ttu-id="ea7be-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7be-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea7be-113">-Name</span></span>
<span data-ttu-id="ea7be-114">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ea7be-114">The resource name.</span></span>

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

### <span data-ttu-id="ea7be-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7be-115">-ResourceGroupName</span></span>
<span data-ttu-id="ea7be-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea7be-116">The resource group name.</span></span>

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

### <span data-ttu-id="ea7be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7be-117">CommonParameters</span></span>
<span data-ttu-id="ea7be-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7be-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea7be-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7be-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea7be-120">INPUTS</span></span>

### <span data-ttu-id="ea7be-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ea7be-121">System.String</span></span>

## <span data-ttu-id="ea7be-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea7be-122">OUTPUTS</span></span>

### <span data-ttu-id="ea7be-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="ea7be-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea7be-124">NOTES</span></span>

## <span data-ttu-id="ea7be-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea7be-125">RELATED LINKS</span></span>
