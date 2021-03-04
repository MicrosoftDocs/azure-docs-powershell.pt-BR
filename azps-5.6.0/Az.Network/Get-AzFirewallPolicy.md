---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: 056a70f6c085f3c0a936f9e144708c7258a3d5c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886002"
---
# <span data-ttu-id="173fb-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="173fb-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="173fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="173fb-102">SYNOPSIS</span></span>
<span data-ttu-id="173fb-103">Obtém uma Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="173fb-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="173fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="173fb-104">SYNTAX</span></span>

### <span data-ttu-id="173fb-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="173fb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="173fb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="173fb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="173fb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="173fb-107">DESCRIPTION</span></span>
<span data-ttu-id="173fb-108">O cmdlet **Get-AzFirewallPolicy** obtém um ou mais Firewalls em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="173fb-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="173fb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="173fb-109">EXAMPLES</span></span>

### <span data-ttu-id="173fb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="173fb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="173fb-111">Este exemplo obter uma política de firewall chamada "firewallPolicy" no grupo de recursos "TestRg"</span><span class="sxs-lookup"><span data-stu-id="173fb-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="173fb-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="173fb-112">PARAMETERS</span></span>

### <span data-ttu-id="173fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="173fb-113">-DefaultProfile</span></span>
<span data-ttu-id="173fb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="173fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="173fb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="173fb-115">-Name</span></span>
<span data-ttu-id="173fb-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="173fb-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="173fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="173fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="173fb-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="173fb-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="173fb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="173fb-119">-ResourceId</span></span>
<span data-ttu-id="173fb-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="173fb-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="173fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="173fb-121">CommonParameters</span></span>
<span data-ttu-id="173fb-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="173fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="173fb-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="173fb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="173fb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="173fb-124">INPUTS</span></span>

### <span data-ttu-id="173fb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="173fb-125">System.String</span></span>

## <span data-ttu-id="173fb-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="173fb-126">OUTPUTS</span></span>

### <span data-ttu-id="173fb-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="173fb-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="173fb-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="173fb-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="173fb-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="173fb-129">NOTES</span></span>

## <span data-ttu-id="173fb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="173fb-130">RELATED LINKS</span></span>
