---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d9ce12176517109ab06f756956c886eae2be9685
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888974"
---
# <span data-ttu-id="11bc8-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="11bc8-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="11bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="11bc8-103">Cria uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="11bc8-103">Creates a service topology.</span></span>

## <span data-ttu-id="11bc8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11bc8-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11bc8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="11bc8-106">O cmdlet **New-AzDeploymentManagerServiceTopology** cria uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="11bc8-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="11bc8-107">Você pode modificar o objeto ServiceTopology retornado localmente e aplicar alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="11bc8-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="11bc8-108">O objeto retornado</span><span class="sxs-lookup"><span data-stu-id="11bc8-108">The returned object</span></span> 

<span data-ttu-id="11bc8-109">O objeto retornado tem um campo ResourceId que pode ser referenciado em um recurso de distribuição para indicar que os serviços declarados nesta topologia de serviço seriam implantados na distribuição.</span><span class="sxs-lookup"><span data-stu-id="11bc8-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="11bc8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11bc8-110">EXAMPLES</span></span>

### <span data-ttu-id="11bc8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11bc8-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="11bc8-112">Este cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local Central US.</span><span class="sxs-lookup"><span data-stu-id="11bc8-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="11bc8-113">A fonte de artefato ResourceId indica que os artefatos necessários para as definições da unidade de serviço nesta topologia precisam ser lidos a partir da fonte de artefato especificada.</span><span class="sxs-lookup"><span data-stu-id="11bc8-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="11bc8-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="11bc8-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="11bc8-115">Este cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local Central US.</span><span class="sxs-lookup"><span data-stu-id="11bc8-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="11bc8-116">A ausência de uma referência de origem de artefato indica que os artefatos necessários para as definições da unidade de serviço nesta topologia seriam fornecidos como URIs SAS absolutos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="11bc8-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="11bc8-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11bc8-117">PARAMETERS</span></span>

### <span data-ttu-id="11bc8-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="11bc8-118">-ArtifactSourceId</span></span>
<span data-ttu-id="11bc8-119">O identificador da origem do artefato, onde os artefatos que com a topologia são armazenados.</span><span class="sxs-lookup"><span data-stu-id="11bc8-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bc8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bc8-120">-DefaultProfile</span></span>
<span data-ttu-id="11bc8-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11bc8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11bc8-122">-Location</span><span class="sxs-lookup"><span data-stu-id="11bc8-122">-Location</span></span>
<span data-ttu-id="11bc8-123">O local da topologia.</span><span class="sxs-lookup"><span data-stu-id="11bc8-123">The location of the topology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bc8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="11bc8-124">-Name</span></span>
<span data-ttu-id="11bc8-125">O nome da topologia.</span><span class="sxs-lookup"><span data-stu-id="11bc8-125">The name of the topology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bc8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11bc8-126">-ResourceGroupName</span></span>
<span data-ttu-id="11bc8-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11bc8-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11bc8-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="11bc8-128">-Tag</span></span>
<span data-ttu-id="11bc8-129">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="11bc8-129">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11bc8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11bc8-130">-Confirm</span></span>
<span data-ttu-id="11bc8-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11bc8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bc8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11bc8-132">-WhatIf</span></span>
<span data-ttu-id="11bc8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11bc8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bc8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11bc8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bc8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bc8-135">CommonParameters</span></span>
<span data-ttu-id="11bc8-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11bc8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bc8-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11bc8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bc8-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11bc8-138">INPUTS</span></span>

### <span data-ttu-id="11bc8-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="11bc8-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="11bc8-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11bc8-140">OUTPUTS</span></span>

### <span data-ttu-id="11bc8-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="11bc8-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="11bc8-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="11bc8-142">NOTES</span></span>

## <span data-ttu-id="11bc8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11bc8-143">RELATED LINKS</span></span>
