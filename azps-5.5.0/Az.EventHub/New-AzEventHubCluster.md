---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117663"
---
# <span data-ttu-id="bbb9b-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="bbb9b-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="bbb9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb9b-103">Cria um novo cluster eventhub dedicado</span><span class="sxs-lookup"><span data-stu-id="bbb9b-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="bbb9b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbb9b-104">SYNTAX</span></span>

### <span data-ttu-id="bbb9b-105">ClusterPropertiesSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbb9b-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbb9b-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbb9b-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb9b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbb9b-107">DESCRIPTION</span></span>
<span data-ttu-id="bbb9b-108">O New-AzEventHubCluster cmdlet cria o cluster eventhub dedicado no determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bbb9b-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="bbb9b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbb9b-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb9b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bbb9b-110">Example 1</span></span>
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

<span data-ttu-id="bbb9b-111">Cria um cluster dedicado 'Eventhub-Cluster-5557' no grupo de recursos 'RSG-Cluster27651' com Localização ao sulcentralus e Capacidade como 1</span><span class="sxs-lookup"><span data-stu-id="bbb9b-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="bbb9b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbb9b-112">PARAMETERS</span></span>

### <span data-ttu-id="bbb9b-113">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="bbb9b-113">-Capacity</span></span>
<span data-ttu-id="bbb9b-114">Capacidade de Cluster (CU), indemnicamente, valor permitido = 1</span><span class="sxs-lookup"><span data-stu-id="bbb9b-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="bbb9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb9b-115">-DefaultProfile</span></span>
<span data-ttu-id="bbb9b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbb9b-117">-Local</span><span class="sxs-lookup"><span data-stu-id="bbb9b-117">-Location</span></span>
<span data-ttu-id="bbb9b-118">Local do Cluster</span><span class="sxs-lookup"><span data-stu-id="bbb9b-118">Location of Cluster</span></span>

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

### <span data-ttu-id="bbb9b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbb9b-119">-Name</span></span>
<span data-ttu-id="bbb9b-120">Nome do Cluster</span><span class="sxs-lookup"><span data-stu-id="bbb9b-120">Cluster Name</span></span>

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

### <span data-ttu-id="bbb9b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb9b-121">-ResourceGroupName</span></span>
<span data-ttu-id="bbb9b-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bbb9b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="bbb9b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbb9b-123">-ResourceId</span></span>
<span data-ttu-id="bbb9b-124">ID do Recurso do Cluster</span><span class="sxs-lookup"><span data-stu-id="bbb9b-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="bbb9b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbb9b-125">-Tag</span></span>
<span data-ttu-id="bbb9b-126">Hashtables que representa marcas de recurso para clusters</span><span class="sxs-lookup"><span data-stu-id="bbb9b-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="bbb9b-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbb9b-127">-Confirm</span></span>
<span data-ttu-id="bbb9b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbb9b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb9b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb9b-129">-WhatIf</span></span>
<span data-ttu-id="bbb9b-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbb9b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbb9b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbb9b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb9b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb9b-132">CommonParameters</span></span>
<span data-ttu-id="bbb9b-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb9b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb9b-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbb9b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb9b-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbb9b-135">INPUTS</span></span>

### <span data-ttu-id="bbb9b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bbb9b-136">System.String</span></span>

### <span data-ttu-id="bbb9b-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bbb9b-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bbb9b-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbb9b-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bbb9b-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbb9b-139">OUTPUTS</span></span>

### <span data-ttu-id="bbb9b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="bbb9b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="bbb9b-141">Notas</span><span class="sxs-lookup"><span data-stu-id="bbb9b-141">NOTES</span></span>

## <span data-ttu-id="bbb9b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbb9b-142">RELATED LINKS</span></span>
