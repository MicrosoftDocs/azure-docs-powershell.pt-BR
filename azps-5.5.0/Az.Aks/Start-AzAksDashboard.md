---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116675"
---
# <span data-ttu-id="1559f-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="1559f-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="1559f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1559f-102">SYNOPSIS</span></span>
<span data-ttu-id="1559f-103">Crie um túnel SSH Deectl para o painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1559f-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="1559f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1559f-104">SYNTAX</span></span>

### <span data-ttu-id="1559f-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1559f-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1559f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1559f-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1559f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1559f-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1559f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1559f-108">DESCRIPTION</span></span>
<span data-ttu-id="1559f-109">Crie um túnel SSH Deectl para o painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1559f-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="1559f-110">O túnel SSH é configurado em um trabalho do PowerShell chamado Kubectl-Tunnel e pode ser encontrado em `Get-Job` execução.</span><span class="sxs-lookup"><span data-stu-id="1559f-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="1559f-111">O túnel deve estar acessível por [http://127.0.0.1:8001](http://127.0.0.1:8001) meio de .</span><span class="sxs-lookup"><span data-stu-id="1559f-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="1559f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1559f-112">EXAMPLES</span></span>

### <span data-ttu-id="1559f-113">Iniciar um túnel SSH e abrir um navegador no painel Desernetes</span><span class="sxs-lookup"><span data-stu-id="1559f-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="1559f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1559f-114">PARAMETERS</span></span>

### <span data-ttu-id="1559f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1559f-115">-DefaultProfile</span></span>
<span data-ttu-id="1559f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1559f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1559f-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="1559f-117">-DisableBrowser</span></span>
<span data-ttu-id="1559f-118">Não abra um navegador após estabelecer o encaminhamento da portaectl.</span><span class="sxs-lookup"><span data-stu-id="1559f-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="1559f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1559f-119">-Id</span></span>
<span data-ttu-id="1559f-120">ID de um cluster de Redenetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="1559f-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1559f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1559f-121">-InputObject</span></span>
<span data-ttu-id="1559f-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1559f-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1559f-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="1559f-123">-ListenPort</span></span>
<span data-ttu-id="1559f-124">A porta de ouvindo do painel.</span><span class="sxs-lookup"><span data-stu-id="1559f-124">The listening port for the dashboard.</span></span> <span data-ttu-id="1559f-125">O valor padrão é 8003.</span><span class="sxs-lookup"><span data-stu-id="1559f-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="1559f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1559f-126">-Name</span></span>
<span data-ttu-id="1559f-127">Nome do cluster Desarnetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="1559f-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="1559f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1559f-128">-PassThru</span></span>
<span data-ttu-id="1559f-129">O Cmdlet retornará o CachorroeTunnelJob se for aprovado.</span><span class="sxs-lookup"><span data-stu-id="1559f-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="1559f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1559f-130">-ResourceGroupName</span></span>
<span data-ttu-id="1559f-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1559f-131">Resource group name</span></span>

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

### <span data-ttu-id="1559f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1559f-132">CommonParameters</span></span>
<span data-ttu-id="1559f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1559f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1559f-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1559f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1559f-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1559f-135">INPUTS</span></span>

### <span data-ttu-id="1559f-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1559f-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="1559f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1559f-137">System.String</span></span>

## <span data-ttu-id="1559f-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="1559f-138">OUTPUTS</span></span>

### <span data-ttu-id="1559f-139">Microsoft.Azure.Commands.Aks.TuneTunnelJob</span><span class="sxs-lookup"><span data-stu-id="1559f-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="1559f-140">Notas</span><span class="sxs-lookup"><span data-stu-id="1559f-140">NOTES</span></span>

## <span data-ttu-id="1559f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1559f-141">RELATED LINKS</span></span>
