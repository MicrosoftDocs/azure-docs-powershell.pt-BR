---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2e0c7f11592238f11f49e82102c6d58c24f8b9fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893207"
---
# <span data-ttu-id="b7b24-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="b7b24-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="b7b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b24-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b24-103">API para atualizar determinadas propriedades do recurso de cluster conectado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-103">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="b7b24-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7b24-104">SYNTAX</span></span>

### <span data-ttu-id="b7b24-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7b24-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7b24-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b7b24-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7b24-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7b24-107">DESCRIPTION</span></span>
<span data-ttu-id="b7b24-108">API para atualizar determinadas propriedades do recurso de cluster conectado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-108">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="b7b24-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7b24-109">EXAMPLES</span></span>

### <span data-ttu-id="b7b24-110">Exemplo 1: atualizar um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="b7b24-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b7b24-111">Este comando atualiza um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="b7b24-112">Exemplo 2: Atualizar um kubernetes conectado por objeto</span><span class="sxs-lookup"><span data-stu-id="b7b24-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="b7b24-113">Este comando atualiza um kubernetes conectado por objeto.</span><span class="sxs-lookup"><span data-stu-id="b7b24-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="b7b24-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7b24-114">PARAMETERS</span></span>

### <span data-ttu-id="b7b24-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7b24-115">-ClusterName</span></span>
<span data-ttu-id="b7b24-116">O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="b7b24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b24-117">-DefaultProfile</span></span>
<span data-ttu-id="b7b24-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7b24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7b24-119">-InputObject</span></span>
<span data-ttu-id="b7b24-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7b24-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7b24-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b24-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7b24-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7b24-122">The name of the resource group.</span></span>
<span data-ttu-id="b7b24-123">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7b24-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b7b24-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7b24-124">-SubscriptionId</span></span>
<span data-ttu-id="b7b24-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b7b24-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b7b24-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7b24-126">-Tag</span></span>
<span data-ttu-id="b7b24-127">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b7b24-127">Resource tags.</span></span>

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

### <span data-ttu-id="b7b24-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7b24-128">-Confirm</span></span>
<span data-ttu-id="b7b24-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7b24-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b24-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b24-130">-WhatIf</span></span>
<span data-ttu-id="b7b24-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b24-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b24-133">CommonParameters</span></span>
<span data-ttu-id="b7b24-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b24-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7b24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b24-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7b24-136">INPUTS</span></span>

### <span data-ttu-id="b7b24-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="b7b24-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="b7b24-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7b24-138">OUTPUTS</span></span>

### <span data-ttu-id="b7b24-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="b7b24-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="b7b24-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7b24-140">NOTES</span></span>

<span data-ttu-id="b7b24-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b7b24-141">ALIASES</span></span>

<span data-ttu-id="b7b24-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="b7b24-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7b24-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b7b24-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7b24-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7b24-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7b24-145">INPUTOBJECT <IConnectedKubernetesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="b7b24-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7b24-146">`[ClusterName <String>]`: O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="b7b24-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="b7b24-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b7b24-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7b24-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7b24-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b7b24-149">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7b24-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7b24-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b7b24-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b7b24-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7b24-151">RELATED LINKS</span></span>

