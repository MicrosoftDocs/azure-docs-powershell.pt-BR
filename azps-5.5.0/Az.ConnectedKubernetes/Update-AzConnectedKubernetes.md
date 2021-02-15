---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115447"
---
# <span data-ttu-id="22c3d-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="22c3d-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="22c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="22c3d-103">API para atualizar determinadas propriedades do recurso de cluster conectado</span><span class="sxs-lookup"><span data-stu-id="22c3d-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="22c3d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22c3d-104">SYNTAX</span></span>

### <span data-ttu-id="22c3d-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="22c3d-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="22c3d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="22c3d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="22c3d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="22c3d-107">DESCRIPTION</span></span>
<span data-ttu-id="22c3d-108">API para atualizar determinadas propriedades do recurso de cluster conectado</span><span class="sxs-lookup"><span data-stu-id="22c3d-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="22c3d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="22c3d-110">Exemplo 1: Atualizar uma rede de rede conectada</span><span class="sxs-lookup"><span data-stu-id="22c3d-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="22c3d-111">Este comando atualiza uma rede conectada.</span><span class="sxs-lookup"><span data-stu-id="22c3d-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="22c3d-112">Exemplo 2: Atualizar uma rede de rede conectada por objeto</span><span class="sxs-lookup"><span data-stu-id="22c3d-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="22c3d-113">Este comando atualiza uma rede conectada por objeto.</span><span class="sxs-lookup"><span data-stu-id="22c3d-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="22c3d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22c3d-114">PARAMETERS</span></span>

### <span data-ttu-id="22c3d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="22c3d-115">-ClusterName</span></span>
<span data-ttu-id="22c3d-116">O nome do cluster Desernetes no qual obter é chamado.</span><span class="sxs-lookup"><span data-stu-id="22c3d-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c3d-117">-DefaultProfile</span></span>
<span data-ttu-id="22c3d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22c3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22c3d-119">-InputObject</span></span>
<span data-ttu-id="22c3d-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="22c3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c3d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c3d-121">-ResourceGroupName</span></span>
<span data-ttu-id="22c3d-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22c3d-122">The name of the resource group.</span></span>
<span data-ttu-id="22c3d-123">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22c3d-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22c3d-124">-SubscriptionId</span></span>
<span data-ttu-id="22c3d-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="22c3d-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="22c3d-126">-Tag</span></span>
<span data-ttu-id="22c3d-127">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="22c3d-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c3d-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="22c3d-128">-Confirm</span></span>
<span data-ttu-id="22c3d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22c3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22c3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c3d-130">-WhatIf</span></span>
<span data-ttu-id="22c3d-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="22c3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22c3d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22c3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22c3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c3d-133">CommonParameters</span></span>
<span data-ttu-id="22c3d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c3d-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22c3d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c3d-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="22c3d-136">INPUTS</span></span>

### <span data-ttu-id="22c3d-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="22c3d-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="22c3d-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="22c3d-138">OUTPUTS</span></span>

### <span data-ttu-id="22c3d-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="22c3d-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="22c3d-140">Notas</span><span class="sxs-lookup"><span data-stu-id="22c3d-140">NOTES</span></span>

<span data-ttu-id="22c3d-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="22c3d-141">ALIASES</span></span>

<span data-ttu-id="22c3d-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="22c3d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="22c3d-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="22c3d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="22c3d-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="22c3d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="22c3d-145">INPUTOBJECT: <IConnectedKubernetesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="22c3d-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="22c3d-146">`[ClusterName <String>]`: o nome do cluster Desarnetes no qual se chama obter.</span><span class="sxs-lookup"><span data-stu-id="22c3d-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="22c3d-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="22c3d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="22c3d-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22c3d-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="22c3d-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="22c3d-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="22c3d-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="22c3d-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="22c3d-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22c3d-151">RELATED LINKS</span></span>

