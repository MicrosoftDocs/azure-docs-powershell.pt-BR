---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115845"
---
# <span data-ttu-id="df71d-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="df71d-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="df71d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df71d-102">SYNOPSIS</span></span>
<span data-ttu-id="df71d-103">Cria uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="df71d-103">Creates a service topology.</span></span>

## <span data-ttu-id="df71d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df71d-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df71d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="df71d-105">DESCRIPTION</span></span>
<span data-ttu-id="df71d-106">O **cmdlet New-AzDeploymentManagerServiceTopology** cria uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="df71d-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="df71d-107">Você pode modificar o objeto ServiceTopology retornado localmente e aplicar alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="df71d-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="df71d-108">O objeto retornado</span><span class="sxs-lookup"><span data-stu-id="df71d-108">The returned object</span></span> 

<span data-ttu-id="df71d-109">O objeto retornado tem um campo ResourceId que pode ser referenciado em um recurso de distribuição para indicar que os serviços declarados nesta topologia de serviço seriam implantados na distribuição.</span><span class="sxs-lookup"><span data-stu-id="df71d-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="df71d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df71d-110">EXAMPLES</span></span>

### <span data-ttu-id="df71d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df71d-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="df71d-112">Este cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="df71d-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="df71d-113">A fonte de artefato ResourceId indica que os artefatos necessários para as definições da unidade de serviço nesta topologia precisam ser lidos a partir da fonte de artefato especificada.</span><span class="sxs-lookup"><span data-stu-id="df71d-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="df71d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="df71d-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="df71d-115">Este cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="df71d-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="df71d-116">A ausência de uma referência de origem de artefato indica que os artefatos necessários para as definições da unidade de serviço nesta topologia seriam fornecidos como URIs SAS absolutas na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="df71d-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="df71d-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df71d-117">PARAMETERS</span></span>

### <span data-ttu-id="df71d-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="df71d-118">-ArtifactSourceId</span></span>
<span data-ttu-id="df71d-119">O identificador da fonte de artefatos, onde os artefatos que comem a topologia são armazenados.</span><span class="sxs-lookup"><span data-stu-id="df71d-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="df71d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df71d-120">-DefaultProfile</span></span>
<span data-ttu-id="df71d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df71d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df71d-122">-Local</span><span class="sxs-lookup"><span data-stu-id="df71d-122">-Location</span></span>
<span data-ttu-id="df71d-123">O local da topologia.</span><span class="sxs-lookup"><span data-stu-id="df71d-123">The location of the topology.</span></span>

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

### <span data-ttu-id="df71d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="df71d-124">-Name</span></span>
<span data-ttu-id="df71d-125">O nome da topologia.</span><span class="sxs-lookup"><span data-stu-id="df71d-125">The name of the topology.</span></span>

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

### <span data-ttu-id="df71d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df71d-126">-ResourceGroupName</span></span>
<span data-ttu-id="df71d-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df71d-127">The resource group.</span></span>

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

### <span data-ttu-id="df71d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="df71d-128">-Tag</span></span>
<span data-ttu-id="df71d-129">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="df71d-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="df71d-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="df71d-130">-Confirm</span></span>
<span data-ttu-id="df71d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df71d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df71d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df71d-132">-WhatIf</span></span>
<span data-ttu-id="df71d-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="df71d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df71d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df71d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df71d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df71d-135">CommonParameters</span></span>
<span data-ttu-id="df71d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df71d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df71d-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df71d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df71d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="df71d-138">INPUTS</span></span>

### <span data-ttu-id="df71d-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="df71d-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df71d-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="df71d-140">OUTPUTS</span></span>

### <span data-ttu-id="df71d-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="df71d-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="df71d-142">Notas</span><span class="sxs-lookup"><span data-stu-id="df71d-142">NOTES</span></span>

## <span data-ttu-id="df71d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df71d-143">RELATED LINKS</span></span>
