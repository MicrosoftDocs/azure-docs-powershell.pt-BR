---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: c31aed5422e9b142690875de242462af64acf799
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112161"
---
# <span data-ttu-id="66b8f-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="66b8f-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="66b8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="66b8f-103">Reinicia uma ou mais instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="66b8f-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="66b8f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66b8f-104">SYNTAX</span></span>

### <span data-ttu-id="66b8f-105">RestartExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="66b8f-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="66b8f-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66b8f-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66b8f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="66b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="66b8f-108">Reinicia uma ou mais instâncias de função em um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="66b8f-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="66b8f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66b8f-109">EXAMPLES</span></span>

### <span data-ttu-id="66b8f-110">Exemplo 1: Reiniciar instâncias de função do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="66b8f-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="66b8f-111">Esse comando reinicia duas instâncias de função ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="66b8f-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="66b8f-112">Exemplo 2: Reiniciar todas as funções do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="66b8f-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="66b8f-113">Esse comando reinicia todas as instâncias de função do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="66b8f-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="66b8f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66b8f-114">PARAMETERS</span></span>

### <span data-ttu-id="66b8f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66b8f-115">-AsJob</span></span>
<span data-ttu-id="66b8f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="66b8f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="66b8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b8f-117">-DefaultProfile</span></span>
<span data-ttu-id="66b8f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66b8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66b8f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66b8f-119">-InputObject</span></span>
<span data-ttu-id="66b8f-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="66b8f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66b8f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="66b8f-121">-Name</span></span>
<span data-ttu-id="66b8f-122">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="66b8f-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b8f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="66b8f-123">-NoWait</span></span>
<span data-ttu-id="66b8f-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="66b8f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="66b8f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66b8f-125">-PassThru</span></span>
<span data-ttu-id="66b8f-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="66b8f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="66b8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="66b8f-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="66b8f-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b8f-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="66b8f-129">-RoleInstance</span></span>
<span data-ttu-id="66b8f-130">Lista de nomes de instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="66b8f-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="66b8f-131">O valor de '\*' significa todas as instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="66b8f-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="66b8f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66b8f-132">-SubscriptionId</span></span>
<span data-ttu-id="66b8f-133">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66b8f-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66b8f-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="66b8f-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66b8f-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="66b8f-135">-Confirm</span></span>
<span data-ttu-id="66b8f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b8f-137">-WhatIf</span></span>
<span data-ttu-id="66b8f-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="66b8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b8f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66b8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b8f-140">CommonParameters</span></span>
<span data-ttu-id="66b8f-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b8f-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66b8f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b8f-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="66b8f-143">INPUTS</span></span>

### <span data-ttu-id="66b8f-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="66b8f-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="66b8f-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="66b8f-145">OUTPUTS</span></span>

### <span data-ttu-id="66b8f-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66b8f-146">System.Boolean</span></span>

## <span data-ttu-id="66b8f-147">Notas</span><span class="sxs-lookup"><span data-stu-id="66b8f-147">NOTES</span></span>

<span data-ttu-id="66b8f-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="66b8f-148">ALIASES</span></span>

<span data-ttu-id="66b8f-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="66b8f-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66b8f-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="66b8f-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66b8f-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66b8f-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66b8f-152">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="66b8f-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66b8f-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="66b8f-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="66b8f-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="66b8f-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66b8f-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="66b8f-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="66b8f-156">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="66b8f-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="66b8f-157">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="66b8f-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="66b8f-158">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66b8f-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66b8f-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="66b8f-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="66b8f-160">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="66b8f-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="66b8f-161">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="66b8f-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="66b8f-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66b8f-162">RELATED LINKS</span></span>

