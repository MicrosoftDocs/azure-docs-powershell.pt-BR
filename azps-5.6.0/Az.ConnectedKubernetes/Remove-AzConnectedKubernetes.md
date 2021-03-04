---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893212"
---
# <span data-ttu-id="609a2-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="609a2-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="609a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609a2-102">SYNOPSIS</span></span>
<span data-ttu-id="609a2-103">Exclua um cluster conectado, removendo o recurso rastreado no Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="609a2-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="609a2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="609a2-104">SYNTAX</span></span>

### <span data-ttu-id="609a2-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="609a2-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="609a2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="609a2-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="609a2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="609a2-107">DESCRIPTION</span></span>
<span data-ttu-id="609a2-108">Exclua um cluster conectado, removendo o recurso rastreado no Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="609a2-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="609a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="609a2-109">EXAMPLES</span></span>

### <span data-ttu-id="609a2-110">Exemplo 1: Remover um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="609a2-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="609a2-111">Este comando remove um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="609a2-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="609a2-112">Exemplo 2: Remover um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="609a2-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="609a2-113">Este comando remove um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="609a2-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="609a2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="609a2-114">PARAMETERS</span></span>

### <span data-ttu-id="609a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="609a2-115">-AsJob</span></span>
<span data-ttu-id="609a2-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="609a2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="609a2-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="609a2-117">-ClusterName</span></span>
<span data-ttu-id="609a2-118">O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="609a2-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609a2-119">-DefaultProfile</span></span>
<span data-ttu-id="609a2-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="609a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="609a2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="609a2-121">-InputObject</span></span>
<span data-ttu-id="609a2-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="609a2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="609a2-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="609a2-123">-KubeConfig</span></span>
<span data-ttu-id="609a2-124">Caminho para o arquivo de configuração kube</span><span class="sxs-lookup"><span data-stu-id="609a2-124">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609a2-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="609a2-125">-KubeContext</span></span>
<span data-ttu-id="609a2-126">Contexto Kubconfig do computador atual</span><span class="sxs-lookup"><span data-stu-id="609a2-126">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609a2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="609a2-127">-NoWait</span></span>
<span data-ttu-id="609a2-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="609a2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="609a2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="609a2-129">-PassThru</span></span>
<span data-ttu-id="609a2-130">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="609a2-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="609a2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609a2-131">-ResourceGroupName</span></span>
<span data-ttu-id="609a2-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="609a2-132">The name of the resource group.</span></span>
<span data-ttu-id="609a2-133">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="609a2-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="609a2-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="609a2-134">-SubscriptionId</span></span>
<span data-ttu-id="609a2-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="609a2-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="609a2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="609a2-136">-Confirm</span></span>
<span data-ttu-id="609a2-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="609a2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609a2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609a2-138">-WhatIf</span></span>
<span data-ttu-id="609a2-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="609a2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609a2-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="609a2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609a2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609a2-141">CommonParameters</span></span>
<span data-ttu-id="609a2-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609a2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609a2-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="609a2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609a2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="609a2-144">INPUTS</span></span>

### <span data-ttu-id="609a2-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="609a2-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="609a2-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="609a2-146">OUTPUTS</span></span>

### <span data-ttu-id="609a2-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="609a2-147">System.Boolean</span></span>

## <span data-ttu-id="609a2-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="609a2-148">NOTES</span></span>

<span data-ttu-id="609a2-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="609a2-149">ALIASES</span></span>

<span data-ttu-id="609a2-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="609a2-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="609a2-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="609a2-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="609a2-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="609a2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="609a2-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="609a2-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="609a2-154">`[ClusterName <String>]`: O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="609a2-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="609a2-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="609a2-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="609a2-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="609a2-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="609a2-157">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="609a2-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="609a2-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="609a2-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="609a2-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="609a2-159">RELATED LINKS</span></span>

