---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112754"
---
# <span data-ttu-id="e0bc6-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="e0bc6-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="e0bc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bc6-103">Cancelar a construção da imagem de longa duração com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="e0bc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0bc6-104">SYNTAX</span></span>

### <span data-ttu-id="e0bc6-105">Cancelar (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0bc6-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0bc6-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0bc6-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0bc6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0bc6-107">DESCRIPTION</span></span>
<span data-ttu-id="e0bc6-108">Cancelar a construção da imagem de longa duração com base no modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="e0bc6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0bc6-109">EXAMPLES</span></span>

### <span data-ttu-id="e0bc6-110">Exemplo 1: parar criação do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="e0bc6-111">Esse comando interrompe a criação de modelos de imagem.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-111">This command stops image template creation.</span></span>

### <span data-ttu-id="e0bc6-112">Exemplo 2: parar criação do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="e0bc6-113">Esse comando interrompe a criação de modelos de imagem.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-113">This command stops image template creation.</span></span>

## <span data-ttu-id="e0bc6-114">OS</span><span class="sxs-lookup"><span data-stu-id="e0bc6-114">PARAMETERS</span></span>

### <span data-ttu-id="e0bc6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0bc6-115">-AsJob</span></span>
<span data-ttu-id="e0bc6-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e0bc6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e0bc6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bc6-117">-DefaultProfile</span></span>
<span data-ttu-id="e0bc6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0bc6-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="e0bc6-119">-ImageTemplateName</span></span>
<span data-ttu-id="e0bc6-120">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-120">The name of the image Template</span></span>

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

### <span data-ttu-id="e0bc6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0bc6-121">-InputObject</span></span>
<span data-ttu-id="e0bc6-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0bc6-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e0bc6-123">-NoWait</span></span>
<span data-ttu-id="e0bc6-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e0bc6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0bc6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0bc6-125">-PassThru</span></span>
<span data-ttu-id="e0bc6-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e0bc6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e0bc6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0bc6-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0bc6-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0bc6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0bc6-129">-SubscriptionId</span></span>
<span data-ttu-id="e0bc6-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0bc6-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0bc6-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0bc6-132">-Confirm</span></span>
<span data-ttu-id="e0bc6-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0bc6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0bc6-134">-WhatIf</span></span>
<span data-ttu-id="e0bc6-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0bc6-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0bc6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bc6-137">CommonParameters</span></span>
<span data-ttu-id="e0bc6-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bc6-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0bc6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bc6-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0bc6-140">INPUTS</span></span>

### <span data-ttu-id="e0bc6-141">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="e0bc6-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="e0bc6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0bc6-142">OUTPUTS</span></span>

### <span data-ttu-id="e0bc6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0bc6-143">System.Boolean</span></span>

## <span data-ttu-id="e0bc6-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0bc6-144">NOTES</span></span>

<span data-ttu-id="e0bc6-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e0bc6-145">ALIASES</span></span>

<span data-ttu-id="e0bc6-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e0bc6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0bc6-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0bc6-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0bc6-149">INPUTobject <IImageBuilderIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e0bc6-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0bc6-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e0bc6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0bc6-151">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="e0bc6-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="e0bc6-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e0bc6-153">`[RunOutputName <String>]`: O nome da saída de execução</span><span class="sxs-lookup"><span data-stu-id="e0bc6-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="e0bc6-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e0bc6-155">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0bc6-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e0bc6-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0bc6-156">RELATED LINKS</span></span>

