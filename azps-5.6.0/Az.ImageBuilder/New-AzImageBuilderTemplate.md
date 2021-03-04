---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 98ef058c8a5110f7b97d794f7ebf41744ac12c2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893281"
---
# <span data-ttu-id="c8ca9-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c8ca9-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c8ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ca9-103">Criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c8ca9-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="c8ca9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8ca9-104">SYNTAX</span></span>

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

## <span data-ttu-id="c8ca9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ca9-106">Criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c8ca9-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="c8ca9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ca9-108">Exemplo 1: Criar um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c8ca9-108">Example 1: Create a virtual machine image template</span></span>
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

<span data-ttu-id="c8ca9-109">Esses comandos criam um modelo de imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="c8ca9-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="c8ca9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8ca9-111">-AsJob</span></span>
<span data-ttu-id="c8ca9-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c8ca9-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c8ca9-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="c8ca9-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="c8ca9-114">Duração máxima a ser esperada durante a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="c8ca9-115">Omita ou especifique 0 para usar o padrão (4 horas).</span><span class="sxs-lookup"><span data-stu-id="c8ca9-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="c8ca9-116">-Customize</span><span class="sxs-lookup"><span data-stu-id="c8ca9-116">-Customize</span></span>
<span data-ttu-id="c8ca9-117">Especifica as propriedades usadas para descrever as etapas de personalização da imagem, como Fonte de imagem etc. Para construir, consulte a seção NOTES para PERSONALIZAR propriedades e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8ca9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ca9-118">-DefaultProfile</span></span>
<span data-ttu-id="c8ca9-119">hideParameter da região As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8ca9-120">-Distribute</span><span class="sxs-lookup"><span data-stu-id="c8ca9-120">-Distribute</span></span>
<span data-ttu-id="c8ca9-121">Os destinos de distribuição para os quais a saída de imagem precisa ir.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="c8ca9-122">Para construir, consulte a seção NOTES para propriedades DISTRIBUTE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8ca9-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="c8ca9-123">-ImageTemplateName</span></span>
<span data-ttu-id="c8ca9-124">O nome do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-124">The name of the image Template.</span></span>

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

### <span data-ttu-id="c8ca9-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="c8ca9-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="c8ca9-126">Hora de término da última executar (UTC).</span><span class="sxs-lookup"><span data-stu-id="c8ca9-126">End time of the last run (UTC).</span></span>

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

### <span data-ttu-id="c8ca9-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="c8ca9-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="c8ca9-128">Informações detalhadas sobre o último estado de executar.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="c8ca9-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="c8ca9-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="c8ca9-130">Estado da última executar.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-130">State of the last run.</span></span>

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

### <span data-ttu-id="c8ca9-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="c8ca9-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="c8ca9-132">Sub-estado da última executar.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-132">Sub-state of the last run.</span></span>

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

### <span data-ttu-id="c8ca9-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="c8ca9-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="c8ca9-134">Hora de início da última corrida (UTC).</span><span class="sxs-lookup"><span data-stu-id="c8ca9-134">Start time of the last run (UTC).</span></span>

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

### <span data-ttu-id="c8ca9-135">-Location</span><span class="sxs-lookup"><span data-stu-id="c8ca9-135">-Location</span></span>
<span data-ttu-id="c8ca9-136">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-136">Resource location.</span></span>

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

### <span data-ttu-id="c8ca9-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c8ca9-137">-NoWait</span></span>
<span data-ttu-id="c8ca9-138">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c8ca9-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c8ca9-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="c8ca9-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="c8ca9-140">Código de erro da falha de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-140">Error code of the provisioning failure.</span></span>

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

### <span data-ttu-id="c8ca9-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="c8ca9-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="c8ca9-142">Mensagem de erro detalhada sobre a falha de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="c8ca9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8ca9-143">-ResourceGroupName</span></span>
<span data-ttu-id="c8ca9-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8ca9-145">-Source</span><span class="sxs-lookup"><span data-stu-id="c8ca9-145">-Source</span></span>
<span data-ttu-id="c8ca9-146">Descreve uma fonte de imagem de máquina virtual para criação, personalização e distribuição.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="c8ca9-147">Para construir, consulte a seção NOTES para propriedades SOURCE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8ca9-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8ca9-148">-SubscriptionId</span></span>
<span data-ttu-id="c8ca9-149">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="c8ca9-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8ca9-150">-Tag</span></span>
<span data-ttu-id="c8ca9-151">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-151">Resource tags.</span></span>

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

### <span data-ttu-id="c8ca9-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="c8ca9-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="c8ca9-153">A id da identidade atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="c8ca9-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="c8ca9-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="c8ca9-155">Tamanho do disco do sistema operacional em GB.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="c8ca9-156">Omita ou especifique 0 para usar o tamanho padrão do disco do sistema operacional do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="c8ca9-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="c8ca9-157">-VMProfileVmSize</span></span>
<span data-ttu-id="c8ca9-158">Tamanho da máquina virtual usada para criar, personalizar e capturar imagens.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="c8ca9-159">Omita ou especifique a cadeia de caracteres vazia para usar o padrão (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="c8ca9-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="c8ca9-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="c8ca9-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="c8ca9-161">ID de recurso de uma sub-rede pré-existente.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="c8ca9-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8ca9-162">-Confirm</span></span>
<span data-ttu-id="c8ca9-163">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8ca9-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8ca9-164">-WhatIf</span></span>
<span data-ttu-id="c8ca9-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8ca9-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8ca9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ca9-167">CommonParameters</span></span>
<span data-ttu-id="c8ca9-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ca9-169">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8ca9-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ca9-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-170">INPUTS</span></span>

## <span data-ttu-id="c8ca9-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-171">OUTPUTS</span></span>

### <span data-ttu-id="c8ca9-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="c8ca9-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="c8ca9-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8ca9-173">NOTES</span></span>

<span data-ttu-id="c8ca9-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c8ca9-174">ALIASES</span></span>

<span data-ttu-id="c8ca9-175">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="c8ca9-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8ca9-176">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8ca9-177">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8ca9-178">CUSTOMIZE <IImageTemplateCustomizer[]>: especifica as propriedades usadas para descrever as etapas de personalização da imagem, como Fonte de imagem etc.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="c8ca9-179">`Type <String>`: O tipo de ferramenta de personalização que você deseja usar na Imagem.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="c8ca9-180">Por exemplo, "Shell" pode ser personalizador de shell</span><span class="sxs-lookup"><span data-stu-id="c8ca9-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="c8ca9-181">`[Name <String>]`: Nome Amigável para fornecer contexto sobre o que essa etapa de personalização faz</span><span class="sxs-lookup"><span data-stu-id="c8ca9-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="c8ca9-182">DISTRIBUTE <IImageTemplateDistributor[]>: a distribuição direciona para onde a saída da imagem precisa ir.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="c8ca9-183">`RunOutputName <String>`: O nome a ser usado para o RunOutput associado.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="c8ca9-184">`Type <String>`: Tipo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="c8ca9-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Marcas que serão aplicadas ao artefato depois que ele tiver sido criado/atualizado pelo distribuidor.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="c8ca9-186">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="c8ca9-187">FONTE : Descreve uma fonte de imagem de máquina <IImageTemplateSource> virtual para criação, personalização e distribuição.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="c8ca9-188">`Type <String>`: Especifica o tipo de imagem de origem com a qual você deseja começar.</span><span class="sxs-lookup"><span data-stu-id="c8ca9-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="c8ca9-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8ca9-189">RELATED LINKS</span></span>

