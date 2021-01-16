---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426673"
---
# <span data-ttu-id="94694-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="94694-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="94694-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94694-102">SYNOPSIS</span></span>
<span data-ttu-id="94694-103">API para registrar um novo cluster K8s e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="94694-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="94694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94694-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94694-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94694-105">DESCRIPTION</span></span>
<span data-ttu-id="94694-106">API para registrar um novo cluster K8s e, assim, criar um recurso controlado no ARM</span><span class="sxs-lookup"><span data-stu-id="94694-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="94694-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94694-107">EXAMPLES</span></span>

### <span data-ttu-id="94694-108">Exemplo 1: criar uma kubernetes conectada</span><span class="sxs-lookup"><span data-stu-id="94694-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="94694-109">Esse comando cria um kubernetes conectado.</span><span class="sxs-lookup"><span data-stu-id="94694-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="94694-110">Exemplo 1: criar uma kubernetes conectada com parâmetros kubeConfig e kubeContext</span><span class="sxs-lookup"><span data-stu-id="94694-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="94694-111">Esse comando cria um kubernetes conectado com parâmetros kubeConfig e kubeContext.</span><span class="sxs-lookup"><span data-stu-id="94694-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="94694-112">OS</span><span class="sxs-lookup"><span data-stu-id="94694-112">PARAMETERS</span></span>

### <span data-ttu-id="94694-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="94694-113">-ClusterName</span></span>
<span data-ttu-id="94694-114">O nome do cluster kubernetes em que Get é chamado.</span><span class="sxs-lookup"><span data-stu-id="94694-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="94694-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94694-115">-DefaultProfile</span></span>
<span data-ttu-id="94694-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94694-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94694-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="94694-117">-KubeConfig</span></span>
<span data-ttu-id="94694-118">Caminho para o arquivo de configuração Kube</span><span class="sxs-lookup"><span data-stu-id="94694-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="94694-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="94694-119">-KubeContext</span></span>
<span data-ttu-id="94694-120">Kubconfig contexto da máquina atual</span><span class="sxs-lookup"><span data-stu-id="94694-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="94694-121">-Local</span><span class="sxs-lookup"><span data-stu-id="94694-121">-Location</span></span>
<span data-ttu-id="94694-122">Localização do cluster</span><span class="sxs-lookup"><span data-stu-id="94694-122">Location of the cluster</span></span>

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

### <span data-ttu-id="94694-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94694-123">-ResourceGroupName</span></span>
<span data-ttu-id="94694-124">O nome do grupo de recursos ao qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="94694-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="94694-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94694-125">-SubscriptionId</span></span>
<span data-ttu-id="94694-126">A ID da assinatura à qual o cluster kubernetes está registrado.</span><span class="sxs-lookup"><span data-stu-id="94694-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="94694-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94694-127">-Confirm</span></span>
<span data-ttu-id="94694-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94694-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94694-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94694-129">-WhatIf</span></span>
<span data-ttu-id="94694-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94694-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94694-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94694-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94694-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94694-132">CommonParameters</span></span>
<span data-ttu-id="94694-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94694-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94694-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94694-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94694-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94694-135">INPUTS</span></span>

## <span data-ttu-id="94694-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94694-136">OUTPUTS</span></span>

### <span data-ttu-id="94694-137">Microsoft. Azure. PowerShell. cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="94694-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="94694-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94694-138">NOTES</span></span>

<span data-ttu-id="94694-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="94694-139">ALIASES</span></span>

## <span data-ttu-id="94694-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94694-140">RELATED LINKS</span></span>

