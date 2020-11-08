---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111913"
---
# <span data-ttu-id="52bc7-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="52bc7-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="52bc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="52bc7-103">Criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="52bc7-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="52bc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52bc7-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52bc7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="52bc7-106">Criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="52bc7-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="52bc7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52bc7-107">EXAMPLES</span></span>

### <span data-ttu-id="52bc7-108">Exemplo 1: criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="52bc7-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="52bc7-109">Este comando cria um modelo de imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52bc7-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="52bc7-110">OS</span><span class="sxs-lookup"><span data-stu-id="52bc7-110">PARAMETERS</span></span>

### <span data-ttu-id="52bc7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52bc7-111">-AsJob</span></span>
<span data-ttu-id="52bc7-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="52bc7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="52bc7-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="52bc7-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="52bc7-114">Duração máxima a esperar durante a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="52bc7-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="52bc7-115">Omita ou especifique 0 para usar o padrão (4 horas).</span><span class="sxs-lookup"><span data-stu-id="52bc7-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="52bc7-116">-Personalizar</span><span class="sxs-lookup"><span data-stu-id="52bc7-116">-Customize</span></span>
<span data-ttu-id="52bc7-117">Especifica as propriedades usadas para descrever as etapas de personalização da imagem, como origem da imagem, etc. Para construir, consulte a seção de anotações para personalizar Propriedades e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52bc7-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bc7-118">-DefaultProfile</span></span>
<span data-ttu-id="52bc7-119">região HideParameter as credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc7-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52bc7-120">-Distribuir</span><span class="sxs-lookup"><span data-stu-id="52bc7-120">-Distribute</span></span>
<span data-ttu-id="52bc7-121">Os destinos de distribuição para os quais a saída da imagem precisa ir.</span><span class="sxs-lookup"><span data-stu-id="52bc7-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="52bc7-122">Para construir, consulte a seção de anotações para distribuir Propriedades e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52bc7-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="52bc7-123">-ImageTemplateName</span></span>
<span data-ttu-id="52bc7-124">O nome do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="52bc7-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="52bc7-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="52bc7-126">Hora de término da última execução (UTC).</span><span class="sxs-lookup"><span data-stu-id="52bc7-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="52bc7-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="52bc7-128">Informações detalhadas sobre o último estado de execução.</span><span class="sxs-lookup"><span data-stu-id="52bc7-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="52bc7-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="52bc7-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="52bc7-130">Estado da última execução.</span><span class="sxs-lookup"><span data-stu-id="52bc7-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="52bc7-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="52bc7-132">Subestado da última execução.</span><span class="sxs-lookup"><span data-stu-id="52bc7-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="52bc7-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="52bc7-134">Hora de início da última execução (UTC).</span><span class="sxs-lookup"><span data-stu-id="52bc7-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-135">-Local</span><span class="sxs-lookup"><span data-stu-id="52bc7-135">-Location</span></span>
<span data-ttu-id="52bc7-136">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="52bc7-136">Resource location.</span></span>

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

### <span data-ttu-id="52bc7-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="52bc7-137">-NoWait</span></span>
<span data-ttu-id="52bc7-138">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="52bc7-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52bc7-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="52bc7-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="52bc7-140">Código de erro da falha de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="52bc7-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="52bc7-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="52bc7-142">Mensagem de erro detalhada sobre a falha de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="52bc7-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="52bc7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bc7-143">-ResourceGroupName</span></span>
<span data-ttu-id="52bc7-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52bc7-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="52bc7-145">-Fonte</span><span class="sxs-lookup"><span data-stu-id="52bc7-145">-Source</span></span>
<span data-ttu-id="52bc7-146">Descreve uma fonte de imagem de máquina virtual para criar, personalizar e distribuir.</span><span class="sxs-lookup"><span data-stu-id="52bc7-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="52bc7-147">Para construir, consulte a seção de notas para propriedades de origem e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="52bc7-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52bc7-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52bc7-148">-SubscriptionId</span></span>
<span data-ttu-id="52bc7-149">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc7-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="52bc7-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="52bc7-150">-Tag</span></span>
<span data-ttu-id="52bc7-151">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="52bc7-151">Resource tags.</span></span>

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

### <span data-ttu-id="52bc7-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="52bc7-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="52bc7-153">A ID da identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="52bc7-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="52bc7-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="52bc7-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="52bc7-155">Tamanho do disco do sistema operacional em GB.</span><span class="sxs-lookup"><span data-stu-id="52bc7-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="52bc7-156">Omita ou especifique 0 para usar o tamanho do disco do sistema operacional padrão do Azure.</span><span class="sxs-lookup"><span data-stu-id="52bc7-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="52bc7-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="52bc7-157">-VMProfileVmSize</span></span>
<span data-ttu-id="52bc7-158">Tamanho da máquina virtual usada para criar, personalizar e capturar imagens.</span><span class="sxs-lookup"><span data-stu-id="52bc7-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="52bc7-159">Omita ou especifique uma cadeia de caracteres vazia para usar o padrão (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="52bc7-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="52bc7-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="52bc7-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="52bc7-161">ID do recurso de uma sub-rede pré-existente.</span><span class="sxs-lookup"><span data-stu-id="52bc7-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="52bc7-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52bc7-162">-Confirm</span></span>
<span data-ttu-id="52bc7-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52bc7-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52bc7-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bc7-164">-WhatIf</span></span>
<span data-ttu-id="52bc7-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52bc7-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52bc7-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52bc7-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52bc7-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bc7-167">CommonParameters</span></span>
<span data-ttu-id="52bc7-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52bc7-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bc7-169">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52bc7-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bc7-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52bc7-170">INPUTS</span></span>

## <span data-ttu-id="52bc7-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52bc7-171">OUTPUTS</span></span>

### <span data-ttu-id="52bc7-172">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="52bc7-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="52bc7-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52bc7-173">NOTES</span></span>

<span data-ttu-id="52bc7-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="52bc7-174">ALIASES</span></span>

<span data-ttu-id="52bc7-175">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="52bc7-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52bc7-176">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="52bc7-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52bc7-177">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52bc7-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52bc7-178">Personalizar <IImageTemplateCustomizer [] >: especifica as propriedades usadas para descrever as etapas de personalização da imagem, como origem da imagem, etc.</span><span class="sxs-lookup"><span data-stu-id="52bc7-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="52bc7-179">`Type <String>`: O tipo de ferramenta de personalização que você deseja usar na imagem.</span><span class="sxs-lookup"><span data-stu-id="52bc7-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="52bc7-180">Por exemplo, "Shell" pode ser personalizador do Shell</span><span class="sxs-lookup"><span data-stu-id="52bc7-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="52bc7-181">`[Name <String>]`: Nome amigável para fornecer contexto sobre o que essa etapa de personalização faz</span><span class="sxs-lookup"><span data-stu-id="52bc7-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="52bc7-182">DISTRIBUIR <IImageTemplateDistributor [] >: os destinos de distribuição onde a saída da imagem precisa ir.</span><span class="sxs-lookup"><span data-stu-id="52bc7-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="52bc7-183">`RunOutputName <String>`: O nome a ser usado para o RunOutput associado.</span><span class="sxs-lookup"><span data-stu-id="52bc7-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="52bc7-184">`Type <String>`: Tipo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="52bc7-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="52bc7-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Marcas que serão aplicadas ao artefato após a criação/atualização do distribuidor.</span><span class="sxs-lookup"><span data-stu-id="52bc7-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="52bc7-186">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="52bc7-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="52bc7-187">FONTE <IImageTemplateSource> : descreve uma fonte de imagem de máquina virtual para construir, personalizar e distribuir.</span><span class="sxs-lookup"><span data-stu-id="52bc7-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="52bc7-188">`Type <String>`: Especifica o tipo de imagem de origem com a qual você deseja começar.</span><span class="sxs-lookup"><span data-stu-id="52bc7-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="52bc7-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52bc7-189">RELATED LINKS</span></span>

