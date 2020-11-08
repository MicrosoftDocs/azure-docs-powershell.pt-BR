---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113373"
---
# <span data-ttu-id="e51b4-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="e51b4-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="e51b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e51b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e51b4-103">Obter informações sobre um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e51b4-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="e51b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e51b4-104">SYNTAX</span></span>

### <span data-ttu-id="e51b4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="e51b4-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e51b4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e51b4-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e51b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e51b4-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e51b4-108">List1</span><span class="sxs-lookup"><span data-stu-id="e51b4-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e51b4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e51b4-109">DESCRIPTION</span></span>
<span data-ttu-id="e51b4-110">Obter informações sobre um modelo de imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e51b4-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="e51b4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e51b4-111">EXAMPLES</span></span>

### <span data-ttu-id="e51b4-112">Exemplo 1: listar todos os modelos sob uma assinatura</span><span class="sxs-lookup"><span data-stu-id="e51b4-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="e51b4-113">Esse comando lista todos os modelos sob uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e51b4-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="e51b4-114">Exemplo 2: listar todos os modelos em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e51b4-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="e51b4-115">Esse comando lista todos os modelos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b4-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="e51b4-116">Exemplo 3: obter um modelo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e51b4-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="e51b4-117">Esse comando obtém um modelo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b4-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="e51b4-118">Exemplo 4: obter um modelo em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e51b4-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="e51b4-119">Esse comando obtém um modelo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b4-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="e51b4-120">OS</span><span class="sxs-lookup"><span data-stu-id="e51b4-120">PARAMETERS</span></span>

### <span data-ttu-id="e51b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51b4-121">-DefaultProfile</span></span>
<span data-ttu-id="e51b4-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e51b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51b4-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="e51b4-123">-ImageTemplateName</span></span>
<span data-ttu-id="e51b4-124">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e51b4-124">The name of the image Template</span></span>

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

### <span data-ttu-id="e51b4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e51b4-125">-InputObject</span></span>
<span data-ttu-id="e51b4-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e51b4-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e51b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="e51b4-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e51b4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e51b4-129">-SubscriptionId</span></span>
<span data-ttu-id="e51b4-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e51b4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e51b4-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e51b4-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e51b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51b4-132">CommonParameters</span></span>
<span data-ttu-id="e51b4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51b4-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e51b4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51b4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e51b4-135">INPUTS</span></span>

### <span data-ttu-id="e51b4-136">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="e51b4-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="e51b4-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e51b4-137">OUTPUTS</span></span>

### <span data-ttu-id="e51b4-138">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="e51b4-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="e51b4-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e51b4-139">NOTES</span></span>

<span data-ttu-id="e51b4-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e51b4-140">ALIASES</span></span>

<span data-ttu-id="e51b4-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e51b4-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e51b4-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e51b4-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e51b4-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e51b4-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e51b4-144">INPUTobject <IImageBuilderIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e51b4-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e51b4-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e51b4-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e51b4-146">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e51b4-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="e51b4-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b4-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e51b4-148">`[RunOutputName <String>]`: O nome da saída de execução</span><span class="sxs-lookup"><span data-stu-id="e51b4-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="e51b4-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e51b4-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e51b4-150">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e51b4-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e51b4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e51b4-151">RELATED LINKS</span></span>

