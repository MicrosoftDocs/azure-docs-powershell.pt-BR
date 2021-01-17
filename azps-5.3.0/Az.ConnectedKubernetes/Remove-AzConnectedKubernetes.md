---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434146"
---
# <span data-ttu-id="b5a35-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="b5a35-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="b5a35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5a35-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a35-103">Exclua um cluster conectado, removendo o recurso controlado no braço do Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="b5a35-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="b5a35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5a35-104">SYNTAX</span></span>

### <span data-ttu-id="b5a35-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="b5a35-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b5a35-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5a35-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a35-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5a35-107">DESCRIPTION</span></span>
<span data-ttu-id="b5a35-108">Exclua um cluster conectado, removendo o recurso controlado no braço do Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="b5a35-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="b5a35-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5a35-109">EXAMPLES</span></span>

### <span data-ttu-id="b5a35-110">Exemplo 1: remover uma kubernetes conectada</span><span class="sxs-lookup"><span data-stu-id="b5a35-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="b5a35-111">Este comando Remove um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="b5a35-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="b5a35-112">Exemplo 2: remover um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="b5a35-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="b5a35-113">Este comando Remove um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="b5a35-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="b5a35-114">OS</span><span class="sxs-lookup"><span data-stu-id="b5a35-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a35-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5a35-115">-AsJob</span></span>
<span data-ttu-id="b5a35-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b5a35-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b5a35-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5a35-117">-ClusterName</span></span>
<span data-ttu-id="b5a35-118">O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="b5a35-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="b5a35-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a35-119">-DefaultProfile</span></span>
<span data-ttu-id="b5a35-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a35-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a35-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5a35-121">-InputObject</span></span>
<span data-ttu-id="b5a35-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b5a35-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5a35-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="b5a35-123">-KubeConfig</span></span>
<span data-ttu-id="b5a35-124">Caminho para o arquivo de configuração Kube</span><span class="sxs-lookup"><span data-stu-id="b5a35-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="b5a35-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="b5a35-125">-KubeContext</span></span>
<span data-ttu-id="b5a35-126">Kubconfig contexto da máquina atual</span><span class="sxs-lookup"><span data-stu-id="b5a35-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="b5a35-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b5a35-127">-NoWait</span></span>
<span data-ttu-id="b5a35-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b5a35-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b5a35-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5a35-129">-PassThru</span></span>
<span data-ttu-id="b5a35-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b5a35-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b5a35-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a35-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5a35-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5a35-132">The name of the resource group.</span></span>
<span data-ttu-id="b5a35-133">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b5a35-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5a35-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5a35-134">-SubscriptionId</span></span>
<span data-ttu-id="b5a35-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b5a35-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5a35-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b5a35-136">-Confirm</span></span>
<span data-ttu-id="b5a35-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a35-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a35-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a35-138">-WhatIf</span></span>
<span data-ttu-id="b5a35-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b5a35-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5a35-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5a35-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a35-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a35-141">CommonParameters</span></span>
<span data-ttu-id="b5a35-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a35-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a35-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5a35-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a35-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5a35-144">INPUTS</span></span>

### <span data-ttu-id="b5a35-145">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="b5a35-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="b5a35-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5a35-146">OUTPUTS</span></span>

### <span data-ttu-id="b5a35-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5a35-147">System.Boolean</span></span>

## <span data-ttu-id="b5a35-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5a35-148">NOTES</span></span>

<span data-ttu-id="b5a35-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b5a35-149">ALIASES</span></span>

<span data-ttu-id="b5a35-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b5a35-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5a35-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b5a35-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5a35-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5a35-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5a35-153">INPUTobject <IConnectedKubernetesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b5a35-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5a35-154">`[ClusterName <String>]`: O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="b5a35-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="b5a35-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b5a35-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5a35-156">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b5a35-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5a35-157">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b5a35-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5a35-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b5a35-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b5a35-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5a35-159">RELATED LINKS</span></span>

