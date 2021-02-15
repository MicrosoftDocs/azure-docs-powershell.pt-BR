---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115183"
---
# <span data-ttu-id="f2316-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f2316-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="f2316-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2316-102">SYNOPSIS</span></span>
<span data-ttu-id="f2316-103">Obtém uma Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f2316-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="f2316-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2316-104">SYNTAX</span></span>

### <span data-ttu-id="f2316-105">GetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2316-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2316-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2316-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2316-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2316-107">DESCRIPTION</span></span>
<span data-ttu-id="f2316-108">O cmdlet **Get-AzFirewallPolicy** obtém um ou mais Firewalls em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f2316-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="f2316-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2316-109">EXAMPLES</span></span>

### <span data-ttu-id="f2316-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2316-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="f2316-111">Este exemplo obterá uma política de firewall chamada "firewallPolicy" no grupo de recursos "TestRg"</span><span class="sxs-lookup"><span data-stu-id="f2316-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="f2316-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2316-112">PARAMETERS</span></span>

### <span data-ttu-id="f2316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2316-113">-DefaultProfile</span></span>
<span data-ttu-id="f2316-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2316-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2316-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2316-115">-Name</span></span>
<span data-ttu-id="f2316-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2316-116">The resource name.</span></span>

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

### <span data-ttu-id="f2316-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2316-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2316-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2316-118">The resource group name.</span></span>

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

### <span data-ttu-id="f2316-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2316-119">-ResourceId</span></span>
<span data-ttu-id="f2316-120">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="f2316-120">The resource Id.</span></span>

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

### <span data-ttu-id="f2316-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2316-121">CommonParameters</span></span>
<span data-ttu-id="f2316-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2316-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2316-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2316-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2316-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2316-124">INPUTS</span></span>

### <span data-ttu-id="f2316-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f2316-125">System.String</span></span>

## <span data-ttu-id="f2316-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2316-126">OUTPUTS</span></span>

### <span data-ttu-id="f2316-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f2316-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="f2316-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f2316-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f2316-129">Notas</span><span class="sxs-lookup"><span data-stu-id="f2316-129">NOTES</span></span>

## <span data-ttu-id="f2316-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2316-130">RELATED LINKS</span></span>
