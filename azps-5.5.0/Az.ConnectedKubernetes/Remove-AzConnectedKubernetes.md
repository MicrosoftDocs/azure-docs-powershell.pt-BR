---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115449"
---
# <span data-ttu-id="49f3a-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="49f3a-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="49f3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="49f3a-103">Exclua um cluster conectado, removendo o recurso rastreado no Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="49f3a-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="49f3a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49f3a-104">SYNTAX</span></span>

### <span data-ttu-id="49f3a-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49f3a-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49f3a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49f3a-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="49f3a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="49f3a-107">DESCRIPTION</span></span>
<span data-ttu-id="49f3a-108">Exclua um cluster conectado, removendo o recurso rastreado no Gerenciador de Recursos do Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="49f3a-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="49f3a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49f3a-109">EXAMPLES</span></span>

### <span data-ttu-id="49f3a-110">Exemplo 1: Remover uma rede de rede conectada</span><span class="sxs-lookup"><span data-stu-id="49f3a-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="49f3a-111">Este comando remove uma rede de rede conectada</span><span class="sxs-lookup"><span data-stu-id="49f3a-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="49f3a-112">Exemplo 2: Remover uma rede de rede conectada por objeto</span><span class="sxs-lookup"><span data-stu-id="49f3a-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="49f3a-113">Este comando remove uma rede de rede conectada por objeto</span><span class="sxs-lookup"><span data-stu-id="49f3a-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="49f3a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49f3a-114">PARAMETERS</span></span>

### <span data-ttu-id="49f3a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49f3a-115">-AsJob</span></span>
<span data-ttu-id="49f3a-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="49f3a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="49f3a-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49f3a-117">-ClusterName</span></span>
<span data-ttu-id="49f3a-118">O nome do cluster Desernetes no qual obter é chamado.</span><span class="sxs-lookup"><span data-stu-id="49f3a-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="49f3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f3a-119">-DefaultProfile</span></span>
<span data-ttu-id="49f3a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49f3a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f3a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49f3a-121">-InputObject</span></span>
<span data-ttu-id="49f3a-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="49f3a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49f3a-123">-IçoeConfig</span><span class="sxs-lookup"><span data-stu-id="49f3a-123">-KubeConfig</span></span>
<span data-ttu-id="49f3a-124">Caminho para o arquivo de configuração de dados</span><span class="sxs-lookup"><span data-stu-id="49f3a-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="49f3a-125">-Ltdacontexto</span><span class="sxs-lookup"><span data-stu-id="49f3a-125">-KubeContext</span></span>
<span data-ttu-id="49f3a-126">Contexto Desconfig do computador atual</span><span class="sxs-lookup"><span data-stu-id="49f3a-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="49f3a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="49f3a-127">-NoWait</span></span>
<span data-ttu-id="49f3a-128">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="49f3a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="49f3a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f3a-129">-PassThru</span></span>
<span data-ttu-id="49f3a-130">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="49f3a-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49f3a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f3a-131">-ResourceGroupName</span></span>
<span data-ttu-id="49f3a-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49f3a-132">The name of the resource group.</span></span>
<span data-ttu-id="49f3a-133">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="49f3a-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="49f3a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49f3a-134">-SubscriptionId</span></span>
<span data-ttu-id="49f3a-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="49f3a-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="49f3a-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="49f3a-136">-Confirm</span></span>
<span data-ttu-id="49f3a-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f3a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f3a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f3a-138">-WhatIf</span></span>
<span data-ttu-id="49f3a-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="49f3a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49f3a-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49f3a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f3a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f3a-141">CommonParameters</span></span>
<span data-ttu-id="49f3a-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f3a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f3a-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49f3a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f3a-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="49f3a-144">INPUTS</span></span>

### <span data-ttu-id="49f3a-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="49f3a-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="49f3a-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="49f3a-146">OUTPUTS</span></span>

### <span data-ttu-id="49f3a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49f3a-147">System.Boolean</span></span>

## <span data-ttu-id="49f3a-148">Notas</span><span class="sxs-lookup"><span data-stu-id="49f3a-148">NOTES</span></span>

<span data-ttu-id="49f3a-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="49f3a-149">ALIASES</span></span>

<span data-ttu-id="49f3a-150">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="49f3a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49f3a-151">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="49f3a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49f3a-152">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49f3a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49f3a-153">INPUTOBJECT: <IConnectedKubernetesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="49f3a-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49f3a-154">`[ClusterName <String>]`: o nome do cluster Desarnetes no qual se chama obter.</span><span class="sxs-lookup"><span data-stu-id="49f3a-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="49f3a-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="49f3a-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49f3a-156">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49f3a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="49f3a-157">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="49f3a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="49f3a-158">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="49f3a-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="49f3a-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49f3a-159">RELATED LINKS</span></span>

