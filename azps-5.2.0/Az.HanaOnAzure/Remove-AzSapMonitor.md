---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258076"
---
# <span data-ttu-id="59714-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="59714-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="59714-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59714-102">SYNOPSIS</span></span>
<span data-ttu-id="59714-103">Exclui um monitor SAP com a assinatura especificada, o grupo de recursos e o nome do monitor.</span><span class="sxs-lookup"><span data-stu-id="59714-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="59714-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59714-104">SYNTAX</span></span>

### <span data-ttu-id="59714-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="59714-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="59714-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="59714-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59714-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59714-107">DESCRIPTION</span></span>
<span data-ttu-id="59714-108">Exclui um monitor SAP com a assinatura especificada, o grupo de recursos e o nome do monitor.</span><span class="sxs-lookup"><span data-stu-id="59714-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="59714-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59714-109">EXAMPLES</span></span>

### <span data-ttu-id="59714-110">Exemplo 1: remover um monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="59714-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="59714-111">Esse comando Remove um monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="59714-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="59714-112">Exemplo 2: remover um monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="59714-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="59714-113">Esse comando Remove um monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="59714-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="59714-114">OS</span><span class="sxs-lookup"><span data-stu-id="59714-114">PARAMETERS</span></span>

### <span data-ttu-id="59714-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59714-115">-AsJob</span></span>
<span data-ttu-id="59714-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="59714-116">Run the command as a job</span></span>

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

### <span data-ttu-id="59714-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59714-117">-DefaultProfile</span></span>
<span data-ttu-id="59714-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59714-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59714-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59714-119">-InputObject</span></span>
<span data-ttu-id="59714-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="59714-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="59714-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="59714-121">-Name</span></span>
<span data-ttu-id="59714-122">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="59714-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59714-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="59714-123">-NoWait</span></span>
<span data-ttu-id="59714-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="59714-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="59714-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59714-125">-PassThru</span></span>
<span data-ttu-id="59714-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="59714-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="59714-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59714-127">-ResourceGroupName</span></span>
<span data-ttu-id="59714-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59714-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="59714-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59714-129">-SubscriptionId</span></span>
<span data-ttu-id="59714-130">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="59714-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59714-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="59714-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="59714-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59714-132">-Confirm</span></span>
<span data-ttu-id="59714-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59714-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59714-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59714-134">-WhatIf</span></span>
<span data-ttu-id="59714-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59714-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59714-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59714-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59714-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59714-137">CommonParameters</span></span>
<span data-ttu-id="59714-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59714-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59714-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59714-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59714-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59714-140">INPUTS</span></span>

### <span data-ttu-id="59714-141">Microsoft. Azure. PowerShell. cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="59714-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="59714-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59714-142">OUTPUTS</span></span>

### <span data-ttu-id="59714-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59714-143">System.Boolean</span></span>

## <span data-ttu-id="59714-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59714-144">NOTES</span></span>

<span data-ttu-id="59714-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="59714-145">ALIASES</span></span>

<span data-ttu-id="59714-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="59714-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59714-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="59714-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59714-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59714-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59714-149">INPUTobject <IHanaOnAzureIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="59714-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59714-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="59714-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59714-151">`[Location <String>]`: O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="59714-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="59714-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="59714-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="59714-153">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="59714-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="59714-154">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59714-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="59714-155">`[ResourceName <String>]`: O nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="59714-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="59714-156">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="59714-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="59714-157">`[Scope <String>]`: O escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="59714-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="59714-158">Recurso pai sendo estendido por identidades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="59714-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="59714-159">`[SubscriptionId <String>]`: ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="59714-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="59714-160">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="59714-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="59714-161">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="59714-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="59714-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59714-162">RELATED LINKS</span></span>

