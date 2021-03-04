---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892926"
---
# <span data-ttu-id="39a68-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="39a68-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="39a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39a68-102">SYNOPSIS</span></span>
<span data-ttu-id="39a68-103">Crie uma nova Implantação ou atualize uma Implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="39a68-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="39a68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="39a68-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="39a68-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="39a68-105">DESCRIPTION</span></span>
<span data-ttu-id="39a68-106">Crie uma nova Implantação ou atualize uma Implantação de saída.</span><span class="sxs-lookup"><span data-stu-id="39a68-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="39a68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39a68-107">EXAMPLES</span></span>

### <span data-ttu-id="39a68-108">Exemplo 1: Exemplo 1: Criar uma implantação de nuvem de mola.</span><span class="sxs-lookup"><span data-stu-id="39a68-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="39a68-109">Crie uma implantação de nuvem de mola.</span><span class="sxs-lookup"><span data-stu-id="39a68-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="39a68-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="39a68-110">PARAMETERS</span></span>

### <span data-ttu-id="39a68-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="39a68-111">-AppName</span></span>
<span data-ttu-id="39a68-112">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="39a68-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="39a68-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39a68-113">-AsJob</span></span>
<span data-ttu-id="39a68-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="39a68-114">Run the command as a job</span></span>

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

### <span data-ttu-id="39a68-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="39a68-115">-Cpu</span></span>
<span data-ttu-id="39a68-116">CPU necessária</span><span class="sxs-lookup"><span data-stu-id="39a68-116">Required CPU</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a68-117">-DefaultProfile</span></span>
<span data-ttu-id="39a68-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39a68-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="39a68-119">-EnvironmentVariable</span></span>
<span data-ttu-id="39a68-120">Coleção de variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="39a68-120">Collection of environment variables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="39a68-121">-JvmOption</span></span>
<span data-ttu-id="39a68-122">Parâmetro JVM</span><span class="sxs-lookup"><span data-stu-id="39a68-122">JVM parameter</span></span>

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

### <span data-ttu-id="39a68-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="39a68-123">-MemoryInGb</span></span>
<span data-ttu-id="39a68-124">Tamanho de memória necessário em GB</span><span class="sxs-lookup"><span data-stu-id="39a68-124">Required Memory size in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-125">-Name</span><span class="sxs-lookup"><span data-stu-id="39a68-125">-Name</span></span>
<span data-ttu-id="39a68-126">O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="39a68-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39a68-127">-NoWait</span></span>
<span data-ttu-id="39a68-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="39a68-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39a68-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a68-129">-ResourceGroupName</span></span>
<span data-ttu-id="39a68-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="39a68-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="39a68-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="39a68-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="39a68-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="39a68-132">-RuntimeVersion</span></span>
<span data-ttu-id="39a68-133">Versão do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="39a68-133">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="39a68-134">-ServiceName</span></span>
<span data-ttu-id="39a68-135">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="39a68-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="39a68-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="39a68-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="39a68-137">Seletor para o artefato a ser usado para a implantação para projetos de vários módulos.</span><span class="sxs-lookup"><span data-stu-id="39a68-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="39a68-138">Esse deve ser o caminho relativo para o módulo/projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="39a68-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="39a68-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="39a68-139">-SourceRelativePath</span></span>
<span data-ttu-id="39a68-140">Caminho relativo do armazenamento que armazena a fonte</span><span class="sxs-lookup"><span data-stu-id="39a68-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="39a68-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="39a68-141">-SourceType</span></span>
<span data-ttu-id="39a68-142">Tipo da fonte carregada</span><span class="sxs-lookup"><span data-stu-id="39a68-142">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="39a68-143">-SourceVersion</span></span>
<span data-ttu-id="39a68-144">Versão da fonte</span><span class="sxs-lookup"><span data-stu-id="39a68-144">Version of the source</span></span>

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

### <span data-ttu-id="39a68-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39a68-145">-SubscriptionId</span></span>
<span data-ttu-id="39a68-146">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="39a68-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="39a68-147">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="39a68-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39a68-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39a68-148">-Confirm</span></span>
<span data-ttu-id="39a68-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39a68-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a68-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a68-150">-WhatIf</span></span>
<span data-ttu-id="39a68-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39a68-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a68-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39a68-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a68-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a68-153">CommonParameters</span></span>
<span data-ttu-id="39a68-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a68-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a68-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39a68-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a68-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39a68-156">INPUTS</span></span>

## <span data-ttu-id="39a68-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="39a68-157">OUTPUTS</span></span>

### <span data-ttu-id="39a68-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="39a68-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="39a68-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="39a68-159">NOTES</span></span>

<span data-ttu-id="39a68-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39a68-160">ALIASES</span></span>

## <span data-ttu-id="39a68-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39a68-161">RELATED LINKS</span></span>

