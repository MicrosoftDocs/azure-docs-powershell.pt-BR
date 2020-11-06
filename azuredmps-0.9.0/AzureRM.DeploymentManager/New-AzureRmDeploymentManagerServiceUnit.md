---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425685"
---
# <span data-ttu-id="44a9b-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="44a9b-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="44a9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="44a9b-103">Cria uma nova unidade de serviço em um serviço em uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="44a9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44a9b-104">SYNTAX</span></span>

### <span data-ttu-id="44a9b-105">ByTopologyAndServiceNames (padrão)</span><span class="sxs-lookup"><span data-stu-id="44a9b-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44a9b-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="44a9b-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44a9b-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="44a9b-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44a9b-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="44a9b-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44a9b-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="44a9b-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44a9b-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44a9b-110">DESCRIPTION</span></span>
<span data-ttu-id="44a9b-111">O cmdlet **New-AzureRmDeploymentManagerServiceUnit** cria um serviço em um serviço em uma topologia de serviço e retorna um objeto que representa essa unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="44a9b-112">Especifique a unidade de serviço por nome, nome do serviço, topologia do serviço na qual ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44a9b-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="44a9b-113">O cmdlet retorna um objeto onunit.</span><span class="sxs-lookup"><span data-stu-id="44a9b-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="44a9b-114">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao serviço usando o cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="44a9b-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="44a9b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44a9b-115">EXAMPLES</span></span>

### <span data-ttu-id="44a9b-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44a9b-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="44a9b-117">Esse cmdlet cria uma nova unidade de serviço com o nome ContosoService2Storage na ContosoResourceGroup abaixo da ContosoService2 do serviço no ContosoServiceTopology de topologia, no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="44a9b-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="44a9b-118">O modelo e os arquivos de parâmetros são definidos como caminhos relativos para o local de origem do artefato referenciado no ContosoServiceTopology de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="44a9b-119">Os recursos definidos neste modelo devem ser implantados no grupo de recursos de destino service2ResourceGroup com o modo de implantação definido como incremental.</span><span class="sxs-lookup"><span data-stu-id="44a9b-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="44a9b-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44a9b-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="44a9b-121">Esse cmdlet cria uma nova unidade de serviço com o nome ContosoService2Storage na ContosoResourceGroup abaixo da ContosoService2 do serviço no ContosoServiceTopology de topologia, no local central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="44a9b-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="44a9b-122">As referências de modelo e parâmetros são fornecidas como URI SAS porque o ResourceId da fonte de artefatos não foi fornecido no ContosoServiceTopology1 de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="44a9b-123">Os recursos definidos neste modelo devem ser implantados no grupo de recursos de destino service2ResourceGroup com o modo de implantação definido como concluir.</span><span class="sxs-lookup"><span data-stu-id="44a9b-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="44a9b-124">OS</span><span class="sxs-lookup"><span data-stu-id="44a9b-124">PARAMETERS</span></span>

### <span data-ttu-id="44a9b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44a9b-125">-AsJob</span></span>
<span data-ttu-id="44a9b-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44a9b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44a9b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a9b-127">-DefaultProfile</span></span>
<span data-ttu-id="44a9b-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44a9b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44a9b-129">-Deploymentmode</span><span class="sxs-lookup"><span data-stu-id="44a9b-129">-DeploymentMode</span></span>
<span data-ttu-id="44a9b-130">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="44a9b-131">-Local</span><span class="sxs-lookup"><span data-stu-id="44a9b-131">-Location</span></span>
<span data-ttu-id="44a9b-132">O local do recurso de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="44a9b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="44a9b-133">-Name</span></span>
<span data-ttu-id="44a9b-134">O nome da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="44a9b-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="44a9b-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="44a9b-136">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="44a9b-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="44a9b-137">-ParametersUri</span></span>
<span data-ttu-id="44a9b-138">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="44a9b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a9b-139">-ResourceGroupName</span></span>
<span data-ttu-id="44a9b-140">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44a9b-140">The resource group.</span></span>

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

### <span data-ttu-id="44a9b-141">-Serviço</span><span class="sxs-lookup"><span data-stu-id="44a9b-141">-Service</span></span>
<span data-ttu-id="44a9b-142">O objeto de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="44a9b-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="44a9b-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="44a9b-143">-ServiceName</span></span>
<span data-ttu-id="44a9b-144">O nome do serviço para o qual esta unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="44a9b-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="44a9b-145">-Objectresourceid</span><span class="sxs-lookup"><span data-stu-id="44a9b-145">-ServiceResourceId</span></span>
<span data-ttu-id="44a9b-146">O identificador do recurso de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="44a9b-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="44a9b-147">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="44a9b-147">-ServiceTopology</span></span>
<span data-ttu-id="44a9b-148">O objeto de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="44a9b-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="44a9b-149">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="44a9b-149">-ServiceTopologyName</span></span>
<span data-ttu-id="44a9b-150">O nome da topologia de serviço na qual esta unidade de serviço faz parte.</span><span class="sxs-lookup"><span data-stu-id="44a9b-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="44a9b-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="44a9b-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="44a9b-152">O identificador de recursos de topologia de serviço no qual a unidade de serviço deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="44a9b-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="44a9b-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="44a9b-153">-Tag</span></span>
<span data-ttu-id="44a9b-154">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="44a9b-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="44a9b-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44a9b-155">-TargetResourceGroup</span></span>
<span data-ttu-id="44a9b-156">Determina o local onde os recursos na unidade de serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="44a9b-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="44a9b-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="44a9b-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="44a9b-158">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="44a9b-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="44a9b-159">-TemplateUri</span></span>
<span data-ttu-id="44a9b-160">O modo de implantação a ser usado ao implantar os recursos na unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="44a9b-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="44a9b-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44a9b-161">-Confirm</span></span>
<span data-ttu-id="44a9b-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44a9b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44a9b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44a9b-163">-WhatIf</span></span>
<span data-ttu-id="44a9b-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44a9b-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44a9b-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44a9b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44a9b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a9b-166">CommonParameters</span></span>
<span data-ttu-id="44a9b-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a9b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a9b-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a9b-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a9b-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44a9b-169">INPUTS</span></span>

### <span data-ttu-id="44a9b-170">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44a9b-170">None</span></span>

## <span data-ttu-id="44a9b-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44a9b-171">OUTPUTS</span></span>

### <span data-ttu-id="44a9b-172">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="44a9b-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="44a9b-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44a9b-173">NOTES</span></span>

## <span data-ttu-id="44a9b-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44a9b-174">RELATED LINKS</span></span>

[<span data-ttu-id="44a9b-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="44a9b-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="44a9b-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="44a9b-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="44a9b-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="44a9b-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)