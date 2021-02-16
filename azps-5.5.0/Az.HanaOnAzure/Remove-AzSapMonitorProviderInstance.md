---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113166"
---
# <span data-ttu-id="3c634-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="3c634-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="3c634-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c634-102">SYNOPSIS</span></span>
<span data-ttu-id="3c634-103">Exclui uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3c634-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="3c634-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c634-104">SYNTAX</span></span>

### <span data-ttu-id="3c634-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c634-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3c634-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c634-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c634-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c634-107">DESCRIPTION</span></span>
<span data-ttu-id="3c634-108">Exclui uma instância de provedor para a assinatura especificada, o grupo de recursos, o nome do SapMonitor e o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3c634-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="3c634-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c634-109">EXAMPLES</span></span>

### <span data-ttu-id="3c634-110">Exemplo 1: remover instância do monitor SAP por nome</span><span class="sxs-lookup"><span data-stu-id="3c634-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="3c634-111">Esse comando remove a instância do monitor SAP por nome.</span><span class="sxs-lookup"><span data-stu-id="3c634-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="3c634-112">Exemplo 2: Remover instância do monitor SAP por objeto</span><span class="sxs-lookup"><span data-stu-id="3c634-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="3c634-113">Esse comando remove a instância do monitor SAP por objeto.</span><span class="sxs-lookup"><span data-stu-id="3c634-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="3c634-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c634-114">PARAMETERS</span></span>

### <span data-ttu-id="3c634-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c634-115">-AsJob</span></span>
<span data-ttu-id="3c634-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3c634-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3c634-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c634-117">-DefaultProfile</span></span>
<span data-ttu-id="3c634-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c634-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c634-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c634-119">-InputObject</span></span>
<span data-ttu-id="3c634-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="3c634-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c634-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c634-121">-Name</span></span>
<span data-ttu-id="3c634-122">Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="3c634-122">Name of the provider instance.</span></span>

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

### <span data-ttu-id="3c634-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c634-123">-NoWait</span></span>
<span data-ttu-id="3c634-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="3c634-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c634-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c634-125">-PassThru</span></span>
<span data-ttu-id="3c634-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="3c634-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c634-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c634-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c634-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c634-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="3c634-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="3c634-129">-SapMonitorName</span></span>
<span data-ttu-id="3c634-130">Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="3c634-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="3c634-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c634-131">-SubscriptionId</span></span>
<span data-ttu-id="3c634-132">ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c634-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c634-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3c634-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c634-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3c634-134">-Confirm</span></span>
<span data-ttu-id="3c634-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c634-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c634-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c634-136">-WhatIf</span></span>
<span data-ttu-id="3c634-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3c634-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c634-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c634-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c634-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c634-139">CommonParameters</span></span>
<span data-ttu-id="3c634-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c634-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c634-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c634-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c634-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="3c634-142">INPUTS</span></span>

### <span data-ttu-id="3c634-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="3c634-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="3c634-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="3c634-144">OUTPUTS</span></span>

### <span data-ttu-id="3c634-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c634-145">System.Boolean</span></span>

## <span data-ttu-id="3c634-146">Notas</span><span class="sxs-lookup"><span data-stu-id="3c634-146">NOTES</span></span>

<span data-ttu-id="3c634-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="3c634-147">ALIASES</span></span>

<span data-ttu-id="3c634-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="3c634-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c634-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3c634-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c634-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c634-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c634-151">INPUTOBJECT: <IHanaOnAzureIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="3c634-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c634-152">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3c634-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c634-153">`[Location <String>]`: o local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="3c634-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="3c634-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome da operação</span><span class="sxs-lookup"><span data-stu-id="3c634-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="3c634-155">`[ProviderInstanceName <String>]`: Nome da instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="3c634-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="3c634-156">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c634-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3c634-157">`[ResourceName <String>]`: o nome do recurso de identidade.</span><span class="sxs-lookup"><span data-stu-id="3c634-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="3c634-158">`[SapMonitorName <String>]`: Nome do recurso de monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="3c634-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="3c634-159">`[Scope <String>]`: o escopo do provedor de recursos do recurso.</span><span class="sxs-lookup"><span data-stu-id="3c634-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="3c634-160">Recurso pai sendo estendido por Identidades Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="3c634-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="3c634-161">`[SubscriptionId <String>]`: ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c634-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c634-162">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3c634-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3c634-163">`[VaultName <String>]`: Nome do cofre</span><span class="sxs-lookup"><span data-stu-id="3c634-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="3c634-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c634-164">RELATED LINKS</span></span>

