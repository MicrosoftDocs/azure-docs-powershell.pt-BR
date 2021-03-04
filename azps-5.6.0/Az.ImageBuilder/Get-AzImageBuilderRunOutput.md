---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893287"
---
# <span data-ttu-id="56d4d-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="56d4d-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="56d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="56d4d-103">Obter a saída de executar especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="56d4d-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="56d4d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56d4d-104">SYNTAX</span></span>

### <span data-ttu-id="56d4d-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56d4d-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56d4d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="56d4d-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56d4d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56d4d-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56d4d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="56d4d-109">Obter a saída de executar especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="56d4d-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="56d4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="56d4d-111">Exemplo 1: Listar todos os resultados de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="56d4d-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="56d4d-112">Este comando lista todos os resultados de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="56d4d-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="56d4d-113">Exemplo 2: Obter um resultado de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="56d4d-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="56d4d-114">Este comando obtém um resultado de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="56d4d-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="56d4d-115">Exemplo 3: Obter um resultado de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="56d4d-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="56d4d-116">Este comando obtém um resultado de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="56d4d-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="56d4d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56d4d-117">PARAMETERS</span></span>

### <span data-ttu-id="56d4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d4d-118">-DefaultProfile</span></span>
<span data-ttu-id="56d4d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56d4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d4d-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="56d4d-120">-ImageTemplateName</span></span>
<span data-ttu-id="56d4d-121">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="56d4d-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d4d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d4d-122">-InputObject</span></span>
<span data-ttu-id="56d4d-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="56d4d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56d4d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d4d-124">-ResourceGroupName</span></span>
<span data-ttu-id="56d4d-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d4d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d4d-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="56d4d-126">-RunOutputName</span></span>
<span data-ttu-id="56d4d-127">O nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="56d4d-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d4d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56d4d-128">-SubscriptionId</span></span>
<span data-ttu-id="56d4d-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56d4d-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="56d4d-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="56d4d-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d4d-131">CommonParameters</span></span>
<span data-ttu-id="56d4d-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d4d-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56d4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d4d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56d4d-134">INPUTS</span></span>

### <span data-ttu-id="56d4d-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="56d4d-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="56d4d-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56d4d-136">OUTPUTS</span></span>

### <span data-ttu-id="56d4d-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="56d4d-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="56d4d-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="56d4d-138">NOTES</span></span>

<span data-ttu-id="56d4d-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56d4d-139">ALIASES</span></span>

<span data-ttu-id="56d4d-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="56d4d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56d4d-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="56d4d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56d4d-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56d4d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56d4d-143">INPUTOBJECT <IImageBuilderIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="56d4d-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56d4d-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="56d4d-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56d4d-145">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="56d4d-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="56d4d-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56d4d-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="56d4d-147">`[RunOutputName <String>]`: O nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="56d4d-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="56d4d-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56d4d-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="56d4d-149">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="56d4d-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="56d4d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d4d-150">RELATED LINKS</span></span>

