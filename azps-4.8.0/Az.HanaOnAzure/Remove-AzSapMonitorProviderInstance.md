---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111756"
---
# <span data-ttu-id="d9782-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="d9782-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="d9782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9782-102">SYNOPSIS</span></span>
<span data-ttu-id="d9782-103">Exclui uma instância do provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d9782-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="d9782-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9782-104">SYNTAX</span></span>

### <span data-ttu-id="d9782-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9782-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d9782-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9782-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9782-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9782-107">DESCRIPTION</span></span>
<span data-ttu-id="d9782-108">Exclui uma instância do provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d9782-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="d9782-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9782-109">EXAMPLES</span></span>

### <span data-ttu-id="d9782-110">Exemplo 1: remover instância do monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="d9782-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="d9782-111">Esse comando Remove a instância do monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="d9782-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="d9782-112">Exemplo 2: remover instância do monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="d9782-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="d9782-113">Esse comando Remove a instância do monitor da SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="d9782-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="d9782-114">OS</span><span class="sxs-lookup"><span data-stu-id="d9782-114">PARAMETERS</span></span>

### <span data-ttu-id="d9782-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9782-115">-AsJob</span></span>
<span data-ttu-id="d9782-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d9782-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d9782-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9782-117">-DefaultProfile</span></span>
<span data-ttu-id="d9782-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9782-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9782-119">-InputObject</span></span>
<span data-ttu-id="d9782-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d9782-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9782-121">-Name</span></span>
<span data-ttu-id="d9782-122">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="d9782-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d9782-123">-NoWait</span></span>
<span data-ttu-id="d9782-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d9782-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9782-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9782-125">-PassThru</span></span>
<span data-ttu-id="d9782-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d9782-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d9782-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9782-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9782-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9782-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="d9782-129">-SapMonitorName</span></span>
<span data-ttu-id="d9782-130">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="d9782-130">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9782-131">-SubscriptionId</span></span>
<span data-ttu-id="d9782-132">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9782-133">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d9782-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9782-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9782-134">-Confirm</span></span>
<span data-ttu-id="d9782-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9782-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9782-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9782-136">-WhatIf</span></span>
<span data-ttu-id="d9782-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9782-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9782-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9782-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9782-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9782-139">CommonParameters</span></span>
<span data-ttu-id="d9782-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9782-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9782-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9782-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9782-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9782-142">INPUTS</span></span>

### <span data-ttu-id="d9782-143">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="d9782-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="d9782-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9782-144">OUTPUTS</span></span>

### <span data-ttu-id="d9782-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9782-145">System.Boolean</span></span>

## <span data-ttu-id="d9782-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9782-146">NOTES</span></span>

<span data-ttu-id="d9782-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d9782-147">ALIASES</span></span>

<span data-ttu-id="d9782-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d9782-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9782-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d9782-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9782-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9782-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9782-151">INPUTobject <IHanaOnAzureIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d9782-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9782-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d9782-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9782-153">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="d9782-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="d9782-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="d9782-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="d9782-155">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="d9782-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="d9782-156">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9782-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d9782-157">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="d9782-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="d9782-158">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="d9782-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="d9782-159">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="d9782-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="d9782-160">Recurso pai sendo estendido por identidades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="d9782-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="d9782-161">`[SubscriptionId <String>]`: ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9782-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9782-162">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d9782-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d9782-163">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="d9782-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="d9782-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9782-164">RELATED LINKS</span></span>

