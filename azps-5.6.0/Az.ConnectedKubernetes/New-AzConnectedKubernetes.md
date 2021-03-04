---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: f6610b86f96602619f12323e7300c66ed39a9f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893215"
---
# <span data-ttu-id="3067e-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="3067e-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="3067e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3067e-102">SYNOPSIS</span></span>
<span data-ttu-id="3067e-103">API para registrar um novo cluster K8s e, assim, criar um recurso rastreado em ARM</span><span class="sxs-lookup"><span data-stu-id="3067e-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="3067e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3067e-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3067e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3067e-105">DESCRIPTION</span></span>
<span data-ttu-id="3067e-106">API para registrar um novo cluster K8s e, assim, criar um recurso rastreado em ARM</span><span class="sxs-lookup"><span data-stu-id="3067e-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="3067e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3067e-107">EXAMPLES</span></span>

### <span data-ttu-id="3067e-108">Exemplo 1: Criar um kubernetes conectado</span><span class="sxs-lookup"><span data-stu-id="3067e-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3067e-109">Este comando cria um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="3067e-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="3067e-110">Exemplo 1: Criar um kubernetes conectado com parâmetros kubeConfig e kubeContext</span><span class="sxs-lookup"><span data-stu-id="3067e-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="3067e-111">Este comando cria um kubernetes conectado com parâmetros kubeConfig e kubeContext.</span><span class="sxs-lookup"><span data-stu-id="3067e-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="3067e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3067e-112">PARAMETERS</span></span>

### <span data-ttu-id="3067e-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3067e-113">-ClusterName</span></span>
<span data-ttu-id="3067e-114">O nome do cluster Kubernetes no qual get é chamado.</span><span class="sxs-lookup"><span data-stu-id="3067e-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3067e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3067e-115">-DefaultProfile</span></span>
<span data-ttu-id="3067e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3067e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3067e-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="3067e-117">-KubeConfig</span></span>
<span data-ttu-id="3067e-118">Caminho para o arquivo de configuração kube</span><span class="sxs-lookup"><span data-stu-id="3067e-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="3067e-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="3067e-119">-KubeContext</span></span>
<span data-ttu-id="3067e-120">Contexto Kubconfig do computador atual</span><span class="sxs-lookup"><span data-stu-id="3067e-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="3067e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="3067e-121">-Location</span></span>
<span data-ttu-id="3067e-122">Local do cluster</span><span class="sxs-lookup"><span data-stu-id="3067e-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3067e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3067e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3067e-124">O nome do grupo de recursos ao qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="3067e-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3067e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3067e-125">-SubscriptionId</span></span>
<span data-ttu-id="3067e-126">A ID da assinatura à qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="3067e-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3067e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3067e-127">-Confirm</span></span>
<span data-ttu-id="3067e-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3067e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3067e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3067e-129">-WhatIf</span></span>
<span data-ttu-id="3067e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3067e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3067e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3067e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3067e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3067e-132">CommonParameters</span></span>
<span data-ttu-id="3067e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3067e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3067e-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3067e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3067e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3067e-135">INPUTS</span></span>

## <span data-ttu-id="3067e-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3067e-136">OUTPUTS</span></span>

### <span data-ttu-id="3067e-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="3067e-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="3067e-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3067e-138">NOTES</span></span>

<span data-ttu-id="3067e-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3067e-139">ALIASES</span></span>

## <span data-ttu-id="3067e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3067e-140">RELATED LINKS</span></span>

