---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114830"
---
# <span data-ttu-id="0d405-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="0d405-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="0d405-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d405-102">SYNOPSIS</span></span>
<span data-ttu-id="0d405-103">Obter a saída de executar especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="0d405-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="0d405-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d405-104">SYNTAX</span></span>

### <span data-ttu-id="0d405-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0d405-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d405-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0d405-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d405-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d405-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d405-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d405-108">DESCRIPTION</span></span>
<span data-ttu-id="0d405-109">Obter a saída de executar especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="0d405-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="0d405-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d405-110">EXAMPLES</span></span>

### <span data-ttu-id="0d405-111">Exemplo 1: Listar todos os resultados de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="0d405-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="0d405-112">Esse comando lista todos os resultados de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="0d405-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="0d405-113">Exemplo 2: Obter um resultado de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="0d405-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="0d405-114">Esse comando obtém um resultado de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="0d405-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="0d405-115">Exemplo 3: Obter um resultado de executar em um modelo</span><span class="sxs-lookup"><span data-stu-id="0d405-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="0d405-116">Esse comando obtém um resultado de executar em um modelo.</span><span class="sxs-lookup"><span data-stu-id="0d405-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="0d405-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d405-117">PARAMETERS</span></span>

### <span data-ttu-id="0d405-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d405-118">-DefaultProfile</span></span>
<span data-ttu-id="0d405-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d405-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d405-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="0d405-120">-ImageTemplateName</span></span>
<span data-ttu-id="0d405-121">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="0d405-121">The name of the image Template</span></span>

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

### <span data-ttu-id="0d405-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d405-122">-InputObject</span></span>
<span data-ttu-id="0d405-123">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0d405-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d405-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d405-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d405-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d405-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d405-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="0d405-126">-RunOutputName</span></span>
<span data-ttu-id="0d405-127">O nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="0d405-127">The name of the run output</span></span>

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

### <span data-ttu-id="0d405-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d405-128">-SubscriptionId</span></span>
<span data-ttu-id="0d405-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0d405-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d405-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0d405-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d405-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d405-131">CommonParameters</span></span>
<span data-ttu-id="0d405-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d405-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d405-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d405-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d405-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d405-134">INPUTS</span></span>

### <span data-ttu-id="0d405-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="0d405-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="0d405-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d405-136">OUTPUTS</span></span>

### <span data-ttu-id="0d405-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="0d405-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="0d405-138">Notas</span><span class="sxs-lookup"><span data-stu-id="0d405-138">NOTES</span></span>

<span data-ttu-id="0d405-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="0d405-139">ALIASES</span></span>

<span data-ttu-id="0d405-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0d405-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d405-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0d405-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d405-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d405-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d405-143">INPUTOBJECT: <IImageBuilderIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0d405-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d405-144">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0d405-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d405-145">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="0d405-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="0d405-146">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d405-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0d405-147">`[RunOutputName <String>]`: o nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="0d405-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="0d405-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0d405-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0d405-149">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0d405-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0d405-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d405-150">RELATED LINKS</span></span>

