---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 1417cc797935a532decf886f0c814ef32deee3aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116567"
---
# <span data-ttu-id="6cd5b-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="6cd5b-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="6cd5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd5b-103">Desligar o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-103">Power off the cloud service.</span></span>
<span data-ttu-id="6cd5b-104">Observe que os recursos ainda estão anexados e você está sendo cobrado pelos recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="6cd5b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cd5b-105">SYNTAX</span></span>

### <span data-ttu-id="6cd5b-106">PowerOff (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6cd5b-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cd5b-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cd5b-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cd5b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cd5b-108">DESCRIPTION</span></span>
<span data-ttu-id="6cd5b-109">Desligar o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-109">Power off the cloud service.</span></span>
<span data-ttu-id="6cd5b-110">Observe que os recursos ainda estão anexados e você está sendo cobrado pelos recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="6cd5b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6cd5b-111">EXAMPLES</span></span>

### <span data-ttu-id="6cd5b-112">Exemplo 1: Interromper o serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="6cd5b-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="6cd5b-113">Esse comando interrompe todas as instâncias de função que pertencem ao serviço de nuvem chamado ContosoCS.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="6cd5b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd5b-114">PARAMETERS</span></span>

### <span data-ttu-id="6cd5b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cd5b-115">-AsJob</span></span>
<span data-ttu-id="6cd5b-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6cd5b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6cd5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd5b-117">-DefaultProfile</span></span>
<span data-ttu-id="6cd5b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cd5b-119">-InputObject</span></span>
<span data-ttu-id="6cd5b-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd5b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cd5b-121">-Name</span></span>
<span data-ttu-id="6cd5b-122">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd5b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6cd5b-123">-NoWait</span></span>
<span data-ttu-id="6cd5b-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="6cd5b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cd5b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cd5b-125">-PassThru</span></span>
<span data-ttu-id="6cd5b-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6cd5b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6cd5b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd5b-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cd5b-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd5b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cd5b-129">-SubscriptionId</span></span>
<span data-ttu-id="6cd5b-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6cd5b-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cd5b-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6cd5b-132">-Confirm</span></span>
<span data-ttu-id="6cd5b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd5b-134">-WhatIf</span></span>
<span data-ttu-id="6cd5b-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd5b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd5b-137">CommonParameters</span></span>
<span data-ttu-id="6cd5b-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd5b-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cd5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd5b-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="6cd5b-140">INPUTS</span></span>

### <span data-ttu-id="6cd5b-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6cd5b-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="6cd5b-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="6cd5b-142">OUTPUTS</span></span>

### <span data-ttu-id="6cd5b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6cd5b-143">System.Boolean</span></span>

## <span data-ttu-id="6cd5b-144">Notas</span><span class="sxs-lookup"><span data-stu-id="6cd5b-144">NOTES</span></span>

<span data-ttu-id="6cd5b-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="6cd5b-145">ALIASES</span></span>

<span data-ttu-id="6cd5b-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6cd5b-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cd5b-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cd5b-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cd5b-149">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6cd5b-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cd5b-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6cd5b-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="6cd5b-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6cd5b-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cd5b-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6cd5b-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="6cd5b-153">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="6cd5b-154">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="6cd5b-155">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6cd5b-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6cd5b-157">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="6cd5b-158">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6cd5b-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="6cd5b-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cd5b-159">RELATED LINKS</span></span>

