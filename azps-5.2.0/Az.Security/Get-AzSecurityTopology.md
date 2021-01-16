---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258946"
---
# <span data-ttu-id="52ef2-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="52ef2-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="52ef2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="52ef2-103">Obtém uma lista de topologias de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="52ef2-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="52ef2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52ef2-104">SYNTAX</span></span>

### <span data-ttu-id="52ef2-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="52ef2-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52ef2-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="52ef2-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52ef2-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="52ef2-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52ef2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52ef2-108">DESCRIPTION</span></span>
<span data-ttu-id="52ef2-109">As topologias de segurança são descobertas automaticamente pela central de segurança do Azure, use esse cmdlet para exibir as topologias de segurança.</span><span class="sxs-lookup"><span data-stu-id="52ef2-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="52ef2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52ef2-110">EXAMPLES</span></span>

### <span data-ttu-id="52ef2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52ef2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="52ef2-112">Exibir todas as topologias de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="52ef2-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="52ef2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52ef2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="52ef2-114">Obter uma topologia de segurança específica</span><span class="sxs-lookup"><span data-stu-id="52ef2-114">Get a specific security topologies</span></span>

## <span data-ttu-id="52ef2-115">OS</span><span class="sxs-lookup"><span data-stu-id="52ef2-115">PARAMETERS</span></span>

### <span data-ttu-id="52ef2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ef2-116">-DefaultProfile</span></span>
<span data-ttu-id="52ef2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52ef2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ef2-118">-Local</span><span class="sxs-lookup"><span data-stu-id="52ef2-118">-Location</span></span>
<span data-ttu-id="52ef2-119">Ponto.</span><span class="sxs-lookup"><span data-stu-id="52ef2-119">Location.</span></span>

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

### <span data-ttu-id="52ef2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="52ef2-120">-Name</span></span>
<span data-ttu-id="52ef2-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52ef2-121">Resource name.</span></span>

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

### <span data-ttu-id="52ef2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ef2-122">-ResourceGroupName</span></span>
<span data-ttu-id="52ef2-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52ef2-123">Resource group name.</span></span>

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

### <span data-ttu-id="52ef2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52ef2-124">-ResourceId</span></span>
<span data-ttu-id="52ef2-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="52ef2-125">Resource ID.</span></span>

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

### <span data-ttu-id="52ef2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ef2-126">CommonParameters</span></span>
<span data-ttu-id="52ef2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ef2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ef2-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ef2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ef2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52ef2-129">INPUTS</span></span>

### <span data-ttu-id="52ef2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52ef2-130">System.String</span></span>

## <span data-ttu-id="52ef2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52ef2-131">OUTPUTS</span></span>

### <span data-ttu-id="52ef2-132">Microsoft. Azure. Commands. Security. Models. Topology. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="52ef2-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="52ef2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52ef2-133">NOTES</span></span>

## <span data-ttu-id="52ef2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52ef2-134">RELATED LINKS</span></span>
