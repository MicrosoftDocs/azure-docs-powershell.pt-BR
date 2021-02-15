---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115299"
---
# <span data-ttu-id="930ac-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="930ac-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="930ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="930ac-102">SYNOPSIS</span></span>
<span data-ttu-id="930ac-103">Cancelar a com build de imagem de longa execução com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="930ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="930ac-104">SYNTAX</span></span>

### <span data-ttu-id="930ac-105">Cancelar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="930ac-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="930ac-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="930ac-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="930ac-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="930ac-107">DESCRIPTION</span></span>
<span data-ttu-id="930ac-108">Cancelar a com build de imagem de longa execução com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="930ac-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="930ac-109">EXAMPLES</span></span>

### <span data-ttu-id="930ac-110">Exemplo 1: Interromper a criação de modelos de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="930ac-111">Esse comando interrompe a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="930ac-111">This command stops image template creation.</span></span>

### <span data-ttu-id="930ac-112">Exemplo 2: Interromper a criação de modelos de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="930ac-113">Esse comando interrompe a criação do modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="930ac-113">This command stops image template creation.</span></span>

## <span data-ttu-id="930ac-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="930ac-114">PARAMETERS</span></span>

### <span data-ttu-id="930ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="930ac-115">-AsJob</span></span>
<span data-ttu-id="930ac-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="930ac-116">Run the command as a job</span></span>

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

### <span data-ttu-id="930ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930ac-117">-DefaultProfile</span></span>
<span data-ttu-id="930ac-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="930ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="930ac-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="930ac-119">-ImageTemplateName</span></span>
<span data-ttu-id="930ac-120">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-120">The name of the image Template</span></span>

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

### <span data-ttu-id="930ac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="930ac-121">-InputObject</span></span>
<span data-ttu-id="930ac-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="930ac-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="930ac-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="930ac-123">-NoWait</span></span>
<span data-ttu-id="930ac-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="930ac-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="930ac-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="930ac-125">-PassThru</span></span>
<span data-ttu-id="930ac-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="930ac-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="930ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="930ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="930ac-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="930ac-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="930ac-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="930ac-129">-SubscriptionId</span></span>
<span data-ttu-id="930ac-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="930ac-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="930ac-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="930ac-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="930ac-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="930ac-132">-Confirm</span></span>
<span data-ttu-id="930ac-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="930ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="930ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="930ac-134">-WhatIf</span></span>
<span data-ttu-id="930ac-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="930ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="930ac-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="930ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="930ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930ac-137">CommonParameters</span></span>
<span data-ttu-id="930ac-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930ac-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930ac-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="930ac-140">INPUTS</span></span>

### <span data-ttu-id="930ac-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="930ac-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="930ac-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="930ac-142">OUTPUTS</span></span>

### <span data-ttu-id="930ac-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="930ac-143">System.Boolean</span></span>

## <span data-ttu-id="930ac-144">Notas</span><span class="sxs-lookup"><span data-stu-id="930ac-144">NOTES</span></span>

<span data-ttu-id="930ac-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="930ac-145">ALIASES</span></span>

<span data-ttu-id="930ac-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="930ac-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="930ac-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="930ac-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="930ac-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="930ac-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="930ac-149">INPUTOBJECT: <IImageBuilderIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="930ac-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="930ac-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="930ac-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="930ac-151">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="930ac-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="930ac-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="930ac-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="930ac-153">`[RunOutputName <String>]`: o nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="930ac-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="930ac-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="930ac-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="930ac-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="930ac-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="930ac-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="930ac-156">RELATED LINKS</span></span>

