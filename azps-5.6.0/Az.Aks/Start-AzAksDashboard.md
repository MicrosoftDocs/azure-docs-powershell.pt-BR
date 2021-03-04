---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5202f4c86d1d83d6e337c61ee6fc0f72a2b031de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891419"
---
# <span data-ttu-id="fe713-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="fe713-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="fe713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe713-102">SYNOPSIS</span></span>
<span data-ttu-id="fe713-103">Crie um túnel SSH Kubectl no painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fe713-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="fe713-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fe713-104">SYNTAX</span></span>

### <span data-ttu-id="fe713-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe713-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe713-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe713-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe713-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe713-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe713-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fe713-108">DESCRIPTION</span></span>
<span data-ttu-id="fe713-109">Crie um túnel SSH Kubectl no painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fe713-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="fe713-110">O túnel SSH é configurado em um trabalho do PowerShell chamado Kubectl-Tunnel e pode ser encontrado executando `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="fe713-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="fe713-111">O túnel deve estar acessível por [http://127.0.0.1:8001](http://127.0.0.1:8001) meio de .</span><span class="sxs-lookup"><span data-stu-id="fe713-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="fe713-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe713-112">EXAMPLES</span></span>

### <span data-ttu-id="fe713-113">Inicie um túnel SSH e abra um navegador para o painel kubernetes</span><span class="sxs-lookup"><span data-stu-id="fe713-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="fe713-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fe713-114">PARAMETERS</span></span>

### <span data-ttu-id="fe713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe713-115">-DefaultProfile</span></span>
<span data-ttu-id="fe713-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe713-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="fe713-117">-DisableBrowser</span></span>
<span data-ttu-id="fe713-118">Não abra um navegador depois de estabelecer o kubectl port-forward.</span><span class="sxs-lookup"><span data-stu-id="fe713-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="fe713-119">-Id</span><span class="sxs-lookup"><span data-stu-id="fe713-119">-Id</span></span>
<span data-ttu-id="fe713-120">ID de um cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="fe713-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe713-121">-InputObject</span></span>
<span data-ttu-id="fe713-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe713-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="fe713-123">-ListenPort</span></span>
<span data-ttu-id="fe713-124">A porta de escuta do painel.</span><span class="sxs-lookup"><span data-stu-id="fe713-124">The listening port for the dashboard.</span></span> <span data-ttu-id="fe713-125">O valor padrão é 8003.</span><span class="sxs-lookup"><span data-stu-id="fe713-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fe713-126">-Name</span></span>
<span data-ttu-id="fe713-127">Nome do cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="fe713-127">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe713-128">-PassThru</span></span>
<span data-ttu-id="fe713-129">O cmdlet retorna o KubeTunnelJob se for passado.</span><span class="sxs-lookup"><span data-stu-id="fe713-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="fe713-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe713-130">-ResourceGroupName</span></span>
<span data-ttu-id="fe713-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fe713-131">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe713-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe713-132">CommonParameters</span></span>
<span data-ttu-id="fe713-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe713-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe713-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe713-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe713-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe713-135">INPUTS</span></span>

### <span data-ttu-id="fe713-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fe713-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="fe713-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fe713-137">System.String</span></span>

## <span data-ttu-id="fe713-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fe713-138">OUTPUTS</span></span>

### <span data-ttu-id="fe713-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="fe713-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="fe713-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="fe713-140">NOTES</span></span>

## <span data-ttu-id="fe713-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe713-141">RELATED LINKS</span></span>
