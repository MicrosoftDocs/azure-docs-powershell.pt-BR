---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceReimage.md
ms.openlocfilehash: 51fa4faa9491e4d119f3c14b1c5b44bee6fdd15e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116904"
---
# <span data-ttu-id="cbf74-101">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="cbf74-101">Invoke-AzCloudServiceReimage</span></span>

## <span data-ttu-id="cbf74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbf74-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf74-103">A operação assíncrona reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalhador.</span><span class="sxs-lookup"><span data-stu-id="cbf74-103">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="cbf74-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbf74-104">SYNTAX</span></span>

### <span data-ttu-id="cbf74-105">ReimageExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbf74-105">ReimageExpanded (Default)</span></span>
```
Invoke-AzCloudServiceReimage -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cbf74-106">ReimageViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cbf74-106">ReimageViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceReimage -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cbf74-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbf74-107">DESCRIPTION</span></span>
<span data-ttu-id="cbf74-108">A operação assíncrona reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalhador.</span><span class="sxs-lookup"><span data-stu-id="cbf74-108">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="cbf74-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbf74-109">EXAMPLES</span></span>

### <span data-ttu-id="cbf74-110">Exemplo 1: Reimage as instâncias de função do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="cbf74-110">Example 1: Reimage role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="cbf74-111">Esse comando reima 2 instâncias de função ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="cbf74-111">This command reimages 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="cbf74-112">Exemplo 2: Reimage todas as funções do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="cbf74-112">Example 2: Reimage all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="cbf74-113">Esse comando reima todas as instâncias de função do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="cbf74-113">This command reimages all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="cbf74-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbf74-114">PARAMETERS</span></span>

### <span data-ttu-id="cbf74-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbf74-115">-AsJob</span></span>
<span data-ttu-id="cbf74-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cbf74-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cbf74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf74-117">-DefaultProfile</span></span>
<span data-ttu-id="cbf74-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf74-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbf74-119">-InputObject</span></span>
<span data-ttu-id="cbf74-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="cbf74-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf74-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbf74-121">-Name</span></span>
<span data-ttu-id="cbf74-122">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="cbf74-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf74-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cbf74-123">-NoWait</span></span>
<span data-ttu-id="cbf74-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="cbf74-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cbf74-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbf74-125">-PassThru</span></span>
<span data-ttu-id="cbf74-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="cbf74-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cbf74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf74-127">-ResourceGroupName</span></span>
<span data-ttu-id="cbf74-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbf74-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf74-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="cbf74-129">-RoleInstance</span></span>
<span data-ttu-id="cbf74-130">Lista de nomes de instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="cbf74-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="cbf74-131">O valor de '\*' significa todas as instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="cbf74-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf74-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbf74-132">-SubscriptionId</span></span>
<span data-ttu-id="cbf74-133">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf74-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cbf74-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbf74-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: ReimageExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf74-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cbf74-135">-Confirm</span></span>
<span data-ttu-id="cbf74-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf74-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf74-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf74-137">-WhatIf</span></span>
<span data-ttu-id="cbf74-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cbf74-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf74-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbf74-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf74-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf74-140">CommonParameters</span></span>
<span data-ttu-id="cbf74-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf74-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf74-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbf74-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf74-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="cbf74-143">INPUTS</span></span>

### <span data-ttu-id="cbf74-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cbf74-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="cbf74-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="cbf74-145">OUTPUTS</span></span>

### <span data-ttu-id="cbf74-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbf74-146">System.Boolean</span></span>

## <span data-ttu-id="cbf74-147">Notas</span><span class="sxs-lookup"><span data-stu-id="cbf74-147">NOTES</span></span>

<span data-ttu-id="cbf74-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="cbf74-148">ALIASES</span></span>

<span data-ttu-id="cbf74-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="cbf74-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbf74-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cbf74-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbf74-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbf74-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbf74-152">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="cbf74-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbf74-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="cbf74-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="cbf74-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="cbf74-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbf74-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="cbf74-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="cbf74-156">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="cbf74-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="cbf74-157">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="cbf74-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="cbf74-158">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf74-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cbf74-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cbf74-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cbf74-160">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="cbf74-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="cbf74-161">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbf74-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="cbf74-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbf74-162">RELATED LINKS</span></span>

