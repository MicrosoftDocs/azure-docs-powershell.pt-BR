---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890344"
---
# <span data-ttu-id="29f32-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="29f32-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="29f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f32-102">SYNOPSIS</span></span>
<span data-ttu-id="29f32-103">Obtém uma lista de Topologias de Segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="29f32-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="29f32-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="29f32-104">SYNTAX</span></span>

### <span data-ttu-id="29f32-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="29f32-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f32-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="29f32-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f32-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29f32-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29f32-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="29f32-108">DESCRIPTION</span></span>
<span data-ttu-id="29f32-109">Topologias de segurança são descobertas automaticamente pelo Centro de Segurança do Azure, use este cmdlet para exibir topologias de segurança.</span><span class="sxs-lookup"><span data-stu-id="29f32-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="29f32-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29f32-110">EXAMPLES</span></span>

### <span data-ttu-id="29f32-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29f32-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="29f32-112">Exibir todas as topologias de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="29f32-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="29f32-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29f32-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="29f32-114">Obter topologias de segurança específicas</span><span class="sxs-lookup"><span data-stu-id="29f32-114">Get a specific security topologies</span></span>

## <span data-ttu-id="29f32-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="29f32-115">PARAMETERS</span></span>

### <span data-ttu-id="29f32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f32-116">-DefaultProfile</span></span>
<span data-ttu-id="29f32-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29f32-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f32-118">-Location</span><span class="sxs-lookup"><span data-stu-id="29f32-118">-Location</span></span>
<span data-ttu-id="29f32-119">Local.</span><span class="sxs-lookup"><span data-stu-id="29f32-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f32-120">-Name</span><span class="sxs-lookup"><span data-stu-id="29f32-120">-Name</span></span>
<span data-ttu-id="29f32-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="29f32-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f32-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f32-122">-ResourceGroupName</span></span>
<span data-ttu-id="29f32-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29f32-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f32-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29f32-124">-ResourceId</span></span>
<span data-ttu-id="29f32-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="29f32-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f32-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f32-126">CommonParameters</span></span>
<span data-ttu-id="29f32-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f32-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f32-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f32-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f32-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29f32-129">INPUTS</span></span>

### <span data-ttu-id="29f32-130">System.String</span><span class="sxs-lookup"><span data-stu-id="29f32-130">System.String</span></span>

## <span data-ttu-id="29f32-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="29f32-131">OUTPUTS</span></span>

### <span data-ttu-id="29f32-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="29f32-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="29f32-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="29f32-133">NOTES</span></span>

## <span data-ttu-id="29f32-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29f32-134">RELATED LINKS</span></span>
