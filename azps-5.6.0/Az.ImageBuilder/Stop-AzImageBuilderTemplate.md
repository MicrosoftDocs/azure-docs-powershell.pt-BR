---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 7b32d3e3b03cfd38ba4cc6eda896eae92674d530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886764"
---
# <span data-ttu-id="590cf-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="590cf-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="590cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="590cf-102">SYNOPSIS</span></span>
<span data-ttu-id="590cf-103">Cancelar a com build de imagem em execução longa com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="590cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="590cf-104">SYNTAX</span></span>

### <span data-ttu-id="590cf-105">Cancelar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="590cf-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="590cf-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="590cf-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="590cf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="590cf-107">DESCRIPTION</span></span>
<span data-ttu-id="590cf-108">Cancelar a com build de imagem em execução longa com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="590cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="590cf-109">EXAMPLES</span></span>

### <span data-ttu-id="590cf-110">Exemplo 1: Interromper a criação do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="590cf-111">Este comando interrompe a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="590cf-111">This command stops image template creation.</span></span>

### <span data-ttu-id="590cf-112">Exemplo 2: Interromper a criação do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="590cf-113">Este comando interrompe a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="590cf-113">This command stops image template creation.</span></span>

## <span data-ttu-id="590cf-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="590cf-114">PARAMETERS</span></span>

### <span data-ttu-id="590cf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="590cf-115">-AsJob</span></span>
<span data-ttu-id="590cf-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="590cf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="590cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590cf-117">-DefaultProfile</span></span>
<span data-ttu-id="590cf-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="590cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="590cf-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="590cf-119">-ImageTemplateName</span></span>
<span data-ttu-id="590cf-120">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="590cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="590cf-121">-InputObject</span></span>
<span data-ttu-id="590cf-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="590cf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="590cf-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="590cf-123">-NoWait</span></span>
<span data-ttu-id="590cf-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="590cf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="590cf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="590cf-125">-PassThru</span></span>
<span data-ttu-id="590cf-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="590cf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="590cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="590cf-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="590cf-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="590cf-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="590cf-129">-SubscriptionId</span></span>
<span data-ttu-id="590cf-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="590cf-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="590cf-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="590cf-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="590cf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="590cf-132">-Confirm</span></span>
<span data-ttu-id="590cf-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="590cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="590cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="590cf-134">-WhatIf</span></span>
<span data-ttu-id="590cf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="590cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="590cf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="590cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="590cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590cf-137">CommonParameters</span></span>
<span data-ttu-id="590cf-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590cf-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="590cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590cf-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="590cf-140">INPUTS</span></span>

### <span data-ttu-id="590cf-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="590cf-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="590cf-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="590cf-142">OUTPUTS</span></span>

### <span data-ttu-id="590cf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="590cf-143">System.Boolean</span></span>

## <span data-ttu-id="590cf-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="590cf-144">NOTES</span></span>

<span data-ttu-id="590cf-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="590cf-145">ALIASES</span></span>

<span data-ttu-id="590cf-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="590cf-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="590cf-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="590cf-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="590cf-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="590cf-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="590cf-149">INPUTOBJECT <IImageBuilderIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="590cf-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="590cf-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="590cf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="590cf-151">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="590cf-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="590cf-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="590cf-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="590cf-153">`[RunOutputName <String>]`: O nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="590cf-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="590cf-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="590cf-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="590cf-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="590cf-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="590cf-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="590cf-156">RELATED LINKS</span></span>

