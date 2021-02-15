---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115301"
---
# <span data-ttu-id="ad873-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="ad873-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="ad873-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad873-102">SYNOPSIS</span></span>
<span data-ttu-id="ad873-103">Criar artefatos a partir de um modelo de imagem existente</span><span class="sxs-lookup"><span data-stu-id="ad873-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ad873-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad873-104">SYNTAX</span></span>

### <span data-ttu-id="ad873-105">Executar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad873-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ad873-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad873-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad873-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad873-107">DESCRIPTION</span></span>
<span data-ttu-id="ad873-108">Criar artefatos a partir de um modelo de imagem existente</span><span class="sxs-lookup"><span data-stu-id="ad873-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ad873-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ad873-109">EXAMPLES</span></span>

### <span data-ttu-id="ad873-110">Exemplo 1: Iniciar um modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ad873-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="ad873-111">Esse comando inicia um modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="ad873-111">This command starts an image template.</span></span>

### <span data-ttu-id="ad873-112">Exemplo 2: Iniciar um modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ad873-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="ad873-113">Esse comando inicia um modelo de imagem.</span><span class="sxs-lookup"><span data-stu-id="ad873-113">This command starts an image template.</span></span>

## <span data-ttu-id="ad873-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad873-114">PARAMETERS</span></span>

### <span data-ttu-id="ad873-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad873-115">-AsJob</span></span>
<span data-ttu-id="ad873-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ad873-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ad873-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad873-117">-DefaultProfile</span></span>
<span data-ttu-id="ad873-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad873-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad873-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ad873-119">-ImageTemplateName</span></span>
<span data-ttu-id="ad873-120">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ad873-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad873-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad873-121">-InputObject</span></span>
<span data-ttu-id="ad873-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ad873-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad873-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad873-123">-NoWait</span></span>
<span data-ttu-id="ad873-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="ad873-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad873-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad873-125">-PassThru</span></span>
<span data-ttu-id="ad873-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="ad873-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad873-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad873-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad873-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad873-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad873-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad873-129">-SubscriptionId</span></span>
<span data-ttu-id="ad873-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad873-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad873-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad873-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad873-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ad873-132">-Confirm</span></span>
<span data-ttu-id="ad873-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad873-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad873-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad873-134">-WhatIf</span></span>
<span data-ttu-id="ad873-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ad873-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad873-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad873-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad873-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad873-137">CommonParameters</span></span>
<span data-ttu-id="ad873-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad873-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad873-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad873-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad873-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="ad873-140">INPUTS</span></span>

### <span data-ttu-id="ad873-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="ad873-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ad873-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="ad873-142">OUTPUTS</span></span>

### <span data-ttu-id="ad873-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad873-143">System.Boolean</span></span>

## <span data-ttu-id="ad873-144">Notas</span><span class="sxs-lookup"><span data-stu-id="ad873-144">NOTES</span></span>

<span data-ttu-id="ad873-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="ad873-145">ALIASES</span></span>

<span data-ttu-id="ad873-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ad873-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad873-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ad873-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad873-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad873-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad873-149">INPUTOBJECT: <IImageBuilderIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="ad873-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad873-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ad873-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad873-151">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ad873-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ad873-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad873-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ad873-153">`[RunOutputName <String>]`: o nome da saída de executar</span><span class="sxs-lookup"><span data-stu-id="ad873-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ad873-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad873-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ad873-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad873-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ad873-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad873-156">RELATED LINKS</span></span>

