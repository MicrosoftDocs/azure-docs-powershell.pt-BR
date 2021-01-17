---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433263"
---
# <span data-ttu-id="de3fb-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="de3fb-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="de3fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="de3fb-103">Obtém uma lista de topologias de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="de3fb-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="de3fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de3fb-104">SYNTAX</span></span>

### <span data-ttu-id="de3fb-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="de3fb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de3fb-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="de3fb-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de3fb-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="de3fb-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de3fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de3fb-108">DESCRIPTION</span></span>
<span data-ttu-id="de3fb-109">As topologias de segurança são descobertas automaticamente pela central de segurança do Azure, use esse cmdlet para exibir as topologias de segurança.</span><span class="sxs-lookup"><span data-stu-id="de3fb-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="de3fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de3fb-110">EXAMPLES</span></span>

### <span data-ttu-id="de3fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de3fb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="de3fb-112">Exibir todas as topologias de segurança em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="de3fb-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="de3fb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de3fb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="de3fb-114">Obter uma topologia de segurança específica</span><span class="sxs-lookup"><span data-stu-id="de3fb-114">Get a specific security topologies</span></span>

## <span data-ttu-id="de3fb-115">OS</span><span class="sxs-lookup"><span data-stu-id="de3fb-115">PARAMETERS</span></span>

### <span data-ttu-id="de3fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3fb-116">-DefaultProfile</span></span>
<span data-ttu-id="de3fb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de3fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de3fb-118">-Local</span><span class="sxs-lookup"><span data-stu-id="de3fb-118">-Location</span></span>
<span data-ttu-id="de3fb-119">Ponto.</span><span class="sxs-lookup"><span data-stu-id="de3fb-119">Location.</span></span>

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

### <span data-ttu-id="de3fb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="de3fb-120">-Name</span></span>
<span data-ttu-id="de3fb-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="de3fb-121">Resource name.</span></span>

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

### <span data-ttu-id="de3fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="de3fb-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de3fb-123">Resource group name.</span></span>

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

### <span data-ttu-id="de3fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de3fb-124">-ResourceId</span></span>
<span data-ttu-id="de3fb-125">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="de3fb-125">Resource ID.</span></span>

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

### <span data-ttu-id="de3fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3fb-126">CommonParameters</span></span>
<span data-ttu-id="de3fb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3fb-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3fb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3fb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de3fb-129">INPUTS</span></span>

### <span data-ttu-id="de3fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de3fb-130">System.String</span></span>

## <span data-ttu-id="de3fb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de3fb-131">OUTPUTS</span></span>

### <span data-ttu-id="de3fb-132">Microsoft. Azure. Commands. Security. Models. Topology. PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="de3fb-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="de3fb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de3fb-133">NOTES</span></span>

## <span data-ttu-id="de3fb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de3fb-134">RELATED LINKS</span></span>
