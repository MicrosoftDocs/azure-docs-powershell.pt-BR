---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116752"
---
# <span data-ttu-id="03831-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="03831-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="03831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03831-102">SYNOPSIS</span></span>
<span data-ttu-id="03831-103">API para registrar um novo cluster K8s e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="03831-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="03831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03831-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03831-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03831-105">DESCRIPTION</span></span>
<span data-ttu-id="03831-106">API para registrar um novo cluster K8s e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="03831-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="03831-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03831-107">EXAMPLES</span></span>

### <span data-ttu-id="03831-108">Exemplo 1: criar uma kubernetes conectada</span><span class="sxs-lookup"><span data-stu-id="03831-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="03831-109">Esse comando cria um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="03831-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="03831-110">Exemplo 1: criar uma kubernetes conectada com parâmetros kubeConfig e kubeContext</span><span class="sxs-lookup"><span data-stu-id="03831-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="03831-111">Esse comando cria um kubernetes conectado com parâmetros kubeConfig e kubeContext.</span><span class="sxs-lookup"><span data-stu-id="03831-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="03831-112">OS</span><span class="sxs-lookup"><span data-stu-id="03831-112">PARAMETERS</span></span>

### <span data-ttu-id="03831-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="03831-113">-ClusterName</span></span>
<span data-ttu-id="03831-114">O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="03831-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="03831-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03831-115">-DefaultProfile</span></span>
<span data-ttu-id="03831-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03831-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03831-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="03831-117">-KubeConfig</span></span>
<span data-ttu-id="03831-118">Caminho para o arquivo de configuração Kube</span><span class="sxs-lookup"><span data-stu-id="03831-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="03831-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="03831-119">-KubeContext</span></span>
<span data-ttu-id="03831-120">Kubconfig contexto da máquina atual</span><span class="sxs-lookup"><span data-stu-id="03831-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="03831-121">-Local</span><span class="sxs-lookup"><span data-stu-id="03831-121">-Location</span></span>
<span data-ttu-id="03831-122">Localização do cluster</span><span class="sxs-lookup"><span data-stu-id="03831-122">Location of the cluster</span></span>

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

### <span data-ttu-id="03831-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03831-123">-ResourceGroupName</span></span>
<span data-ttu-id="03831-124">O nome do grupo de recursos ao qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="03831-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="03831-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03831-125">-SubscriptionId</span></span>
<span data-ttu-id="03831-126">A ID da assinatura à qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="03831-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="03831-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03831-127">-Confirm</span></span>
<span data-ttu-id="03831-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03831-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03831-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03831-129">-WhatIf</span></span>
<span data-ttu-id="03831-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03831-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03831-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03831-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03831-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03831-132">CommonParameters</span></span>
<span data-ttu-id="03831-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03831-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03831-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03831-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03831-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03831-135">INPUTS</span></span>

## <span data-ttu-id="03831-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03831-136">OUTPUTS</span></span>

### <span data-ttu-id="03831-137">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="03831-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="03831-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03831-138">NOTES</span></span>

<span data-ttu-id="03831-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="03831-139">ALIASES</span></span>

## <span data-ttu-id="03831-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03831-140">RELATED LINKS</span></span>

