---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284096"
---
# <span data-ttu-id="5ba39-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5ba39-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="5ba39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ba39-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba39-103">Obtém uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5ba39-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="5ba39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ba39-104">SYNTAX</span></span>

### <span data-ttu-id="5ba39-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5ba39-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ba39-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ba39-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba39-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ba39-107">DESCRIPTION</span></span>
<span data-ttu-id="5ba39-108">O cmdlet **Get-AzFirewallPolicy** Obtém um ou mais firewalls em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5ba39-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="5ba39-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ba39-109">EXAMPLES</span></span>

### <span data-ttu-id="5ba39-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ba39-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="5ba39-111">Este exemplo obtém uma política de firewall chamada "firewallPolicy" no grupo de recursos "TestRg"</span><span class="sxs-lookup"><span data-stu-id="5ba39-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="5ba39-112">OS</span><span class="sxs-lookup"><span data-stu-id="5ba39-112">PARAMETERS</span></span>

### <span data-ttu-id="5ba39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba39-113">-DefaultProfile</span></span>
<span data-ttu-id="5ba39-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba39-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ba39-115">-Name</span></span>
<span data-ttu-id="5ba39-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5ba39-116">The resource name.</span></span>

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

### <span data-ttu-id="5ba39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba39-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ba39-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ba39-118">The resource group name.</span></span>

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

### <span data-ttu-id="5ba39-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ba39-119">-ResourceId</span></span>
<span data-ttu-id="5ba39-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="5ba39-120">The resource Id.</span></span>

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

### <span data-ttu-id="5ba39-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba39-121">CommonParameters</span></span>
<span data-ttu-id="5ba39-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba39-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba39-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ba39-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba39-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ba39-124">INPUTS</span></span>

### <span data-ttu-id="5ba39-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba39-125">System.String</span></span>

## <span data-ttu-id="5ba39-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ba39-126">OUTPUTS</span></span>

### <span data-ttu-id="5ba39-127">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="5ba39-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="5ba39-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5ba39-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5ba39-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ba39-129">NOTES</span></span>

## <span data-ttu-id="5ba39-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ba39-130">RELATED LINKS</span></span>
