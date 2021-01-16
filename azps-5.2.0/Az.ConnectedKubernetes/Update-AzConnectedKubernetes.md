---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263884"
---
# <span data-ttu-id="62183-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="62183-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="62183-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62183-102">SYNOPSIS</span></span>
<span data-ttu-id="62183-103">API para atualizar determinadas propriedades do recurso de cluster conectado</span><span class="sxs-lookup"><span data-stu-id="62183-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="62183-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62183-104">SYNTAX</span></span>

### <span data-ttu-id="62183-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="62183-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62183-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="62183-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62183-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62183-107">DESCRIPTION</span></span>
<span data-ttu-id="62183-108">API para atualizar determinadas propriedades do recurso de cluster conectado</span><span class="sxs-lookup"><span data-stu-id="62183-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="62183-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62183-109">EXAMPLES</span></span>

### <span data-ttu-id="62183-110">Exemplo 1: atualizar uma kubernetes conectada</span><span class="sxs-lookup"><span data-stu-id="62183-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="62183-111">Esse comando atualiza um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="62183-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="62183-112">Exemplo 2: atualizar uma kubernetes conectada por objeto</span><span class="sxs-lookup"><span data-stu-id="62183-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="62183-113">Esse comando atualiza um kubernetes conectado por objeto.</span><span class="sxs-lookup"><span data-stu-id="62183-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="62183-114">OS</span><span class="sxs-lookup"><span data-stu-id="62183-114">PARAMETERS</span></span>

### <span data-ttu-id="62183-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="62183-115">-ClusterName</span></span>
<span data-ttu-id="62183-116">O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="62183-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="62183-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62183-117">-DefaultProfile</span></span>
<span data-ttu-id="62183-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62183-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62183-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62183-119">-InputObject</span></span>
<span data-ttu-id="62183-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="62183-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62183-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62183-121">-ResourceGroupName</span></span>
<span data-ttu-id="62183-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62183-122">The name of the resource group.</span></span>
<span data-ttu-id="62183-123">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62183-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="62183-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62183-124">-SubscriptionId</span></span>
<span data-ttu-id="62183-125">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="62183-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="62183-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="62183-126">-Tag</span></span>
<span data-ttu-id="62183-127">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="62183-127">Resource tags.</span></span>

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

### <span data-ttu-id="62183-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62183-128">-Confirm</span></span>
<span data-ttu-id="62183-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62183-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62183-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62183-130">-WhatIf</span></span>
<span data-ttu-id="62183-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62183-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62183-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62183-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62183-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62183-133">CommonParameters</span></span>
<span data-ttu-id="62183-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62183-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62183-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62183-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62183-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62183-136">INPUTS</span></span>

### <span data-ttu-id="62183-137">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="62183-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="62183-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62183-138">OUTPUTS</span></span>

### <span data-ttu-id="62183-139">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="62183-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="62183-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62183-140">NOTES</span></span>

<span data-ttu-id="62183-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62183-141">ALIASES</span></span>

<span data-ttu-id="62183-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="62183-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62183-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="62183-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62183-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62183-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62183-145">INPUTobject <IConnectedKubernetesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="62183-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62183-146">`[ClusterName <String>]`: O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="62183-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="62183-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="62183-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62183-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62183-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="62183-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="62183-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="62183-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="62183-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="62183-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62183-151">RELATED LINKS</span></span>

