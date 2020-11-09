---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280615"
---
# <span data-ttu-id="b8354-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b8354-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b8354-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8354-102">SYNOPSIS</span></span>
<span data-ttu-id="b8354-103">Cria uma unidade de serviço na topologia de serviço e serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="b8354-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="b8354-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8354-104">SYNTAX</span></span>

### <span data-ttu-id="b8354-105">ByTopologyAndServiceNames (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8354-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8354-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b8354-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8354-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b8354-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8354-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="b8354-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8354-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b8354-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8354-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8354-110">DESCRIPTION</span></span>
<span data-ttu-id="b8354-111">O cmdlet **New-AzDeploymentManagerServiceUnit** cria um serviço em um serviço em uma topologia de serviço e retorna um objeto que representa essa unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="b8354-112">Especifique a unidade de serviço por nome, nome do serviço, topologia do serviço na qual ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8354-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="b8354-113">O cmdlet retorna um objeto onunit.</span><span class="sxs-lookup"><span data-stu-id="b8354-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="b8354-114">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao serviço usando o cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="b8354-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="b8354-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8354-115">EXAMPLES</span></span>

### <span data-ttu-id="b8354-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8354-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="b8354-117">Esse cmdlet cria uma nova unidade de serviço com o nome ContosoService2Storage na ContosoResourceGroup abaixo da ContosoService2 do serviço no ContosoServiceTopology de topologia, no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b8354-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b8354-118">O modelo e os arquivos de parâmetros são definidos como caminhos relativos para o local de origem do artefato referenciado no ContosoServiceTopology de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="b8354-119">Os recursos definidos neste modelo devem ser implantados no grupo de recursos de destino service2ResourceGroup com o modo de implantação definido como incremental.</span><span class="sxs-lookup"><span data-stu-id="b8354-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="b8354-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8354-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="b8354-121">Esse cmdlet cria uma nova unidade de serviço com o nome ContosoService2Storage na ContosoResourceGroup abaixo da ContosoService2 do serviço no ContosoServiceTopology de topologia, no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="b8354-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b8354-122">As referências de modelo e parâmetros são fornecidas como URI SAS porque o ResourceId da fonte de artefatos não foi fornecido no ContosoServiceTopology1 de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="b8354-123">Os recursos definidos neste modelo devem ser implantados no grupo de recursos de destino service2ResourceGroup com o modo de implantação definido como concluir.</span><span class="sxs-lookup"><span data-stu-id="b8354-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="b8354-124">OS</span><span class="sxs-lookup"><span data-stu-id="b8354-124">PARAMETERS</span></span>

### <span data-ttu-id="b8354-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8354-125">-AsJob</span></span>
<span data-ttu-id="b8354-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b8354-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8354-127">-DefaultProfile</span></span>
<span data-ttu-id="b8354-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8354-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8354-129">-Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="b8354-129">-DeploymentMode</span></span>
<span data-ttu-id="b8354-130">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-131">-Local</span><span class="sxs-lookup"><span data-stu-id="b8354-131">-Location</span></span>
<span data-ttu-id="b8354-132">O local do recurso de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="b8354-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8354-133">-Name</span></span>
<span data-ttu-id="b8354-134">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b8354-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b8354-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="b8354-136">O caminho para o arquivo de parâmetros relativo à origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="b8354-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="b8354-137">Requer que o Artefatote seja referenciado no imtopology.</span><span class="sxs-lookup"><span data-stu-id="b8354-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="b8354-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="b8354-138">-ParametersUri</span></span>
<span data-ttu-id="b8354-139">O URI da SAS para o arquivo de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b8354-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="b8354-140">Se ArtifactSourceId foi referenciado no imtopology, especifique o caminho relativo usando ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="b8354-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="b8354-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8354-141">-ResourceGroupName</span></span>
<span data-ttu-id="b8354-142">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8354-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b8354-143">-ServiceName</span></span>
<span data-ttu-id="b8354-144">O nome do serviço para o qual esta unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="b8354-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="b8354-145">-ServiceObject</span></span>
<span data-ttu-id="b8354-146">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="b8354-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-147">-Objectresourceid</span><span class="sxs-lookup"><span data-stu-id="b8354-147">-ServiceResourceId</span></span>
<span data-ttu-id="b8354-148">O identificador do recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="b8354-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-149">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="b8354-149">-ServiceTopologyName</span></span>
<span data-ttu-id="b8354-150">O nome da topologia de serviço na qual esta unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="b8354-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-151">-Imtopologyobject</span><span class="sxs-lookup"><span data-stu-id="b8354-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="b8354-152">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="b8354-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b8354-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b8354-154">O identificador de recursos de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="b8354-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8354-155">-Marca</span><span class="sxs-lookup"><span data-stu-id="b8354-155">-Tag</span></span>
<span data-ttu-id="b8354-156">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8354-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b8354-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b8354-157">-TargetResourceGroup</span></span>
<span data-ttu-id="b8354-158">Determina o local onde os recursos na unidade de serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="b8354-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="b8354-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b8354-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="b8354-160">O caminho para o arquivo de modelo relativo à fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="b8354-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="b8354-161">Requer que o Artefatote seja referenciado no imtopology.</span><span class="sxs-lookup"><span data-stu-id="b8354-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="b8354-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b8354-162">-TemplateUri</span></span>
<span data-ttu-id="b8354-163">O URI da SAS para o arquivo de modelo.</span><span class="sxs-lookup"><span data-stu-id="b8354-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="b8354-164">Se ArtifactSourceId foi referenciado no imtopology, especifique o caminho relativo usando TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="b8354-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="b8354-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8354-165">-Confirm</span></span>
<span data-ttu-id="b8354-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8354-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8354-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8354-167">-WhatIf</span></span>
<span data-ttu-id="b8354-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8354-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8354-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8354-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8354-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8354-170">CommonParameters</span></span>
<span data-ttu-id="b8354-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8354-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8354-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8354-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8354-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8354-173">INPUTS</span></span>

### <span data-ttu-id="b8354-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8354-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b8354-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8354-175">OUTPUTS</span></span>

### <span data-ttu-id="b8354-176">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b8354-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b8354-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8354-177">NOTES</span></span>

## <span data-ttu-id="b8354-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8354-178">RELATED LINKS</span></span>
