---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943344"
---
# <span data-ttu-id="73383-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="73383-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="73383-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73383-102">SYNOPSIS</span></span>
<span data-ttu-id="73383-103">Obtém um grupo de regras de política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="73383-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="73383-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73383-104">SYNTAX</span></span>

### <span data-ttu-id="73383-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="73383-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73383-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73383-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73383-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73383-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73383-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73383-108">DESCRIPTION</span></span>
<span data-ttu-id="73383-109">O cmdlet **Get-AzFirewallPolicyRuleCollectionGroup** Obtém o RuleCollectionGroup mencionado de uma política de firewall</span><span class="sxs-lookup"><span data-stu-id="73383-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="73383-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73383-110">EXAMPLES</span></span>

### <span data-ttu-id="73383-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="73383-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="73383-112">Este exemplo obtém o grupo de regras de regra na política de firewall $fp</span><span class="sxs-lookup"><span data-stu-id="73383-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="73383-113">OS</span><span class="sxs-lookup"><span data-stu-id="73383-113">PARAMETERS</span></span>

### <span data-ttu-id="73383-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73383-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="73383-115">Política de firewall.</span><span class="sxs-lookup"><span data-stu-id="73383-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73383-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="73383-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="73383-117">O nome da política de firewall</span><span class="sxs-lookup"><span data-stu-id="73383-117">The Firewall policy name</span></span>

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

### <span data-ttu-id="73383-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73383-118">-DefaultProfile</span></span>
<span data-ttu-id="73383-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73383-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73383-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73383-120">-Name</span></span>
<span data-ttu-id="73383-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="73383-121">The resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73383-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73383-122">-ResourceGroupName</span></span>
<span data-ttu-id="73383-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73383-123">The resource group name.</span></span>

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

### <span data-ttu-id="73383-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73383-124">-ResourceId</span></span>
<span data-ttu-id="73383-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="73383-125">The resource Id.</span></span>

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

### <span data-ttu-id="73383-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73383-126">CommonParameters</span></span>
<span data-ttu-id="73383-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73383-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73383-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73383-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73383-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73383-129">INPUTS</span></span>

### <span data-ttu-id="73383-130">System. String</span><span class="sxs-lookup"><span data-stu-id="73383-130">System.String</span></span>

### <span data-ttu-id="73383-131">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="73383-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="73383-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73383-132">OUTPUTS</span></span>

### <span data-ttu-id="73383-133">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="73383-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="73383-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73383-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="73383-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73383-135">NOTES</span></span>

## <span data-ttu-id="73383-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73383-136">RELATED LINKS</span></span>
