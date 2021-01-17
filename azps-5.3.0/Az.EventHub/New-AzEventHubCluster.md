---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429394"
---
# <span data-ttu-id="239ed-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="239ed-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="239ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="239ed-102">SYNOPSIS</span></span>
<span data-ttu-id="239ed-103">Cria um novo cluster exclusivo do eventhub</span><span class="sxs-lookup"><span data-stu-id="239ed-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="239ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="239ed-104">SYNTAX</span></span>

### <span data-ttu-id="239ed-105">ClusterPropertiesSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="239ed-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="239ed-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="239ed-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239ed-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="239ed-107">DESCRIPTION</span></span>
<span data-ttu-id="239ed-108">O cmdlet New-AzEventHubCluster cria o cluster do eventhub dedicado no grupo de recursos específico</span><span class="sxs-lookup"><span data-stu-id="239ed-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="239ed-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="239ed-109">EXAMPLES</span></span>

### <span data-ttu-id="239ed-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="239ed-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="239ed-111">Cria o cluster dedicado "Eventhub-cluster-5557" no grupo de Cluster27651 "RSG-" com o local southcentralus e a capacidade como 1</span><span class="sxs-lookup"><span data-stu-id="239ed-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="239ed-112">OS</span><span class="sxs-lookup"><span data-stu-id="239ed-112">PARAMETERS</span></span>

### <span data-ttu-id="239ed-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="239ed-113">-Capacity</span></span>
<span data-ttu-id="239ed-114">Capacidade do cluster (RECOR), curerntrly, valor permitido = 1</span><span class="sxs-lookup"><span data-stu-id="239ed-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239ed-115">-DefaultProfile</span></span>
<span data-ttu-id="239ed-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="239ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239ed-117">-Local</span><span class="sxs-lookup"><span data-stu-id="239ed-117">-Location</span></span>
<span data-ttu-id="239ed-118">Local do cluster</span><span class="sxs-lookup"><span data-stu-id="239ed-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="239ed-119">-Name</span></span>
<span data-ttu-id="239ed-120">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="239ed-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="239ed-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="239ed-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="239ed-123">-ResourceId</span></span>
<span data-ttu-id="239ed-124">ID do recurso do cluster</span><span class="sxs-lookup"><span data-stu-id="239ed-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="239ed-125">-Tag</span></span>
<span data-ttu-id="239ed-126">Hashtables que representam marcas de recursos para clusters</span><span class="sxs-lookup"><span data-stu-id="239ed-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="239ed-127">-Confirm</span></span>
<span data-ttu-id="239ed-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="239ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239ed-129">-WhatIf</span></span>
<span data-ttu-id="239ed-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="239ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="239ed-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="239ed-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239ed-132">CommonParameters</span></span>
<span data-ttu-id="239ed-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239ed-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="239ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239ed-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="239ed-135">INPUTS</span></span>

### <span data-ttu-id="239ed-136">System. String</span><span class="sxs-lookup"><span data-stu-id="239ed-136">System.String</span></span>

### <span data-ttu-id="239ed-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="239ed-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="239ed-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="239ed-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="239ed-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="239ed-139">OUTPUTS</span></span>

### <span data-ttu-id="239ed-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="239ed-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="239ed-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="239ed-141">NOTES</span></span>

## <span data-ttu-id="239ed-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="239ed-142">RELATED LINKS</span></span>
