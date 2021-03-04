---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: 82730525f6330336be72e922881d743345515926
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893285"
---
# <span data-ttu-id="963cd-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="963cd-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="963cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="963cd-102">SYNOPSIS</span></span>
<span data-ttu-id="963cd-103">Obter informações sobre um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="963cd-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="963cd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="963cd-104">SYNTAX</span></span>

### <span data-ttu-id="963cd-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="963cd-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="963cd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="963cd-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="963cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="963cd-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="963cd-108">List1</span><span class="sxs-lookup"><span data-stu-id="963cd-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="963cd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="963cd-109">DESCRIPTION</span></span>
<span data-ttu-id="963cd-110">Obter informações sobre um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="963cd-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="963cd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="963cd-111">EXAMPLES</span></span>

### <span data-ttu-id="963cd-112">Exemplo 1: Listar todos os modelos em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="963cd-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="963cd-113">Este comando lista todos os modelos em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="963cd-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="963cd-114">Exemplo 2: Listar todos os modelos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="963cd-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="963cd-115">Este comando lista todos os modelos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="963cd-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="963cd-116">Exemplo 3: Obter um modelo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="963cd-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="963cd-117">Este comando obtém um modelo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="963cd-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="963cd-118">Exemplo 4: Obter um modelo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="963cd-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="963cd-119">Este comando obtém um modelo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="963cd-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="963cd-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="963cd-120">PARAMETERS</span></span>

### <span data-ttu-id="963cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963cd-121">-DefaultProfile</span></span>
<span data-ttu-id="963cd-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="963cd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963cd-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="963cd-123">-ImageTemplateName</span></span>
<span data-ttu-id="963cd-124">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="963cd-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963cd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="963cd-125">-InputObject</span></span>
<span data-ttu-id="963cd-126">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="963cd-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="963cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="963cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="963cd-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="963cd-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963cd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="963cd-129">-SubscriptionId</span></span>
<span data-ttu-id="963cd-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="963cd-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="963cd-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="963cd-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963cd-132">CommonParameters</span></span>
<span data-ttu-id="963cd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="963cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963cd-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="963cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963cd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="963cd-135">INPUTS</span></span>

### <span data-ttu-id="963cd-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="963cd-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="963cd-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="963cd-137">OUTPUTS</span></span>

### <span data-ttu-id="963cd-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="963cd-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="963cd-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="963cd-139">NOTES</span></span>

<span data-ttu-id="963cd-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="963cd-140">ALIASES</span></span>

<span data-ttu-id="963cd-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="963cd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="963cd-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="963cd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="963cd-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="963cd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="963cd-144">INPUTOBJECT <IImageBuilderIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="963cd-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="963cd-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="963cd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="963cd-146">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="963cd-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="963cd-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="963cd-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="963cd-148">`[RunOutputName <String>]`: O nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="963cd-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="963cd-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="963cd-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="963cd-150">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="963cd-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="963cd-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="963cd-151">RELATED LINKS</span></span>

