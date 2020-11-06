---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426048"
---
# <span data-ttu-id="e0012-101">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e0012-101">New-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="e0012-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0012-102">SYNOPSIS</span></span>
<span data-ttu-id="e0012-103">Cria uma nova topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0012-103">Creates a new service topology.</span></span>

## <span data-ttu-id="e0012-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0012-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0012-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0012-105">DESCRIPTION</span></span>
<span data-ttu-id="e0012-106">O cmdlet **New-AzureRmDeploymentManagerServiceTopology** cria uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0012-106">The **New-AzureRmDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="e0012-107">Você pode modificar o objeto imtopology retornado localmente e, em seguida, aplicar as alterações à topologia usando o cmdlet Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="e0012-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="e0012-108">O objeto retornado</span><span class="sxs-lookup"><span data-stu-id="e0012-108">The returned object</span></span> 

<span data-ttu-id="e0012-109">O objeto retornado tem um campo ResourceId que pode ser referenciado em um recurso de distribuição para indicar que os serviços declarados nesta topologia de serviço seriam implantados na distribuição.</span><span class="sxs-lookup"><span data-stu-id="e0012-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="e0012-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0012-110">EXAMPLES</span></span>

### <span data-ttu-id="e0012-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0012-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="e0012-112">Esse cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="e0012-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="e0012-113">O ResourceId da fonte de artefatos indica que os artefatos necessários para as definições da unidade de serviço nessa topologia precisam ser lidos a partir da fonte de artefatos especificada.</span><span class="sxs-lookup"><span data-stu-id="e0012-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="e0012-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e0012-114">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="e0012-115">Esse cmdlet cria uma nova topologia de serviço no grupo de recursos ContosoResourceGroup com o nome ContosoServiceTopology e no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="e0012-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="e0012-116">A ausência de uma referência da fonte de artefatos indica que os artefatos necessários para as definições da unidade de serviço nessa topologia seriam fornecidos como URIs de SAS absoluta na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0012-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="e0012-117">OS</span><span class="sxs-lookup"><span data-stu-id="e0012-117">PARAMETERS</span></span>

### <span data-ttu-id="e0012-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="e0012-118">-ArtifactSourceId</span></span>
<span data-ttu-id="e0012-119">O identificador da origem do artefato, em que os artefatos que compõem a topologia são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e0012-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="e0012-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0012-120">-DefaultProfile</span></span>
<span data-ttu-id="e0012-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0012-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0012-122">-Local</span><span class="sxs-lookup"><span data-stu-id="e0012-122">-Location</span></span>
<span data-ttu-id="e0012-123">O local da topologia.</span><span class="sxs-lookup"><span data-stu-id="e0012-123">The location of the topology.</span></span>

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

### <span data-ttu-id="e0012-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0012-124">-Name</span></span>
<span data-ttu-id="e0012-125">O nome da topologia.</span><span class="sxs-lookup"><span data-stu-id="e0012-125">The name of the topology.</span></span>

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

### <span data-ttu-id="e0012-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0012-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0012-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0012-127">The resource group.</span></span>

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

### <span data-ttu-id="e0012-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="e0012-128">-Tag</span></span>
<span data-ttu-id="e0012-129">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0012-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e0012-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0012-130">-Confirm</span></span>
<span data-ttu-id="e0012-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0012-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0012-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0012-132">-WhatIf</span></span>
<span data-ttu-id="e0012-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0012-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0012-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0012-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0012-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0012-135">CommonParameters</span></span>
<span data-ttu-id="e0012-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0012-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0012-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0012-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0012-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0012-138">INPUTS</span></span>

### <span data-ttu-id="e0012-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e0012-139">None</span></span>

## <span data-ttu-id="e0012-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0012-140">OUTPUTS</span></span>

### <span data-ttu-id="e0012-141">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="e0012-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="e0012-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0012-142">NOTES</span></span>

## <span data-ttu-id="e0012-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0012-143">RELATED LINKS</span></span>

[<span data-ttu-id="e0012-144">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e0012-144">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e0012-145">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e0012-145">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e0012-146">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e0012-146">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)