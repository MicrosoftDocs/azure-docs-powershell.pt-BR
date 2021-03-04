---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: aa9f128021aba1dff08f1c8757c8135676ddc003
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888377"
---
# <span data-ttu-id="6b633-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="6b633-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="6b633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b633-102">SYNOPSIS</span></span>
<span data-ttu-id="6b633-103">Reconstruir Instâncias de Função reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalho e inicializa os recursos de armazenamento usados por elas.</span><span class="sxs-lookup"><span data-stu-id="6b633-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="6b633-104">Se você não quiser inicializar recursos de armazenamento, poderá usar Instâncias de Função reimage.</span><span class="sxs-lookup"><span data-stu-id="6b633-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="6b633-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b633-105">SYNTAX</span></span>

### <span data-ttu-id="6b633-106">RebuildExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="6b633-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6b633-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6b633-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b633-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b633-108">DESCRIPTION</span></span>
<span data-ttu-id="6b633-109">Reconstruir Instâncias de Função reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalho e inicializa os recursos de armazenamento usados por elas.</span><span class="sxs-lookup"><span data-stu-id="6b633-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="6b633-110">Se você não quiser inicializar recursos de armazenamento, poderá usar Instâncias de Função reimage.</span><span class="sxs-lookup"><span data-stu-id="6b633-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="6b633-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b633-111">EXAMPLES</span></span>

### <span data-ttu-id="6b633-112">Exemplo 1: Recriar instâncias de função do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="6b633-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="6b633-113">Este comando recria duas instâncias de função ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6b633-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="6b633-114">Exemplo 2: reconstruir todas as funções do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="6b633-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="6b633-115">Este comando reconstrói todas as instâncias de função do serviço de nuvem chamada ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6b633-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6b633-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b633-116">PARAMETERS</span></span>

### <span data-ttu-id="6b633-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b633-117">-AsJob</span></span>
<span data-ttu-id="6b633-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6b633-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6b633-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6b633-119">-CloudServiceName</span></span>
<span data-ttu-id="6b633-120">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6b633-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b633-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b633-121">-DefaultProfile</span></span>
<span data-ttu-id="6b633-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b633-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b633-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b633-123">-InputObject</span></span>
<span data-ttu-id="6b633-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6b633-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b633-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b633-125">-NoWait</span></span>
<span data-ttu-id="6b633-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6b633-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b633-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b633-127">-PassThru</span></span>
<span data-ttu-id="6b633-128">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6b633-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b633-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b633-129">-ResourceGroupName</span></span>
<span data-ttu-id="6b633-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b633-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b633-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="6b633-131">-RoleInstance</span></span>
<span data-ttu-id="6b633-132">Lista de nomes de instâncias de função de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6b633-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="6b633-133">O valor de '\*' significa todas as instâncias de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="6b633-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="6b633-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b633-134">-SubscriptionId</span></span>
<span data-ttu-id="6b633-135">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b633-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6b633-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6b633-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b633-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b633-137">-Confirm</span></span>
<span data-ttu-id="6b633-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b633-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b633-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b633-139">-WhatIf</span></span>
<span data-ttu-id="6b633-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b633-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b633-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b633-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b633-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b633-142">CommonParameters</span></span>
<span data-ttu-id="6b633-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b633-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b633-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b633-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b633-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b633-145">INPUTS</span></span>

### <span data-ttu-id="6b633-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6b633-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="6b633-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b633-147">OUTPUTS</span></span>

### <span data-ttu-id="6b633-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b633-148">System.Boolean</span></span>

## <span data-ttu-id="6b633-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b633-149">NOTES</span></span>

<span data-ttu-id="6b633-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6b633-150">ALIASES</span></span>

<span data-ttu-id="6b633-151">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6b633-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b633-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6b633-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b633-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b633-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b633-154">INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6b633-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b633-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6b633-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="6b633-156">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b633-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b633-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6b633-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="6b633-158">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="6b633-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="6b633-159">`[RoleName <String>]`: Nome da função.</span><span class="sxs-lookup"><span data-stu-id="6b633-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="6b633-160">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b633-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6b633-161">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6b633-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6b633-162">`[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="6b633-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="6b633-163">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="6b633-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="6b633-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b633-164">RELATED LINKS</span></span>

