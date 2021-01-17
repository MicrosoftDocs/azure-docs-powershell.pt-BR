---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429021"
---
# <span data-ttu-id="ca74c-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="ca74c-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="ca74c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca74c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca74c-103">Crie um encapsulamento SSH Kubectl para o painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ca74c-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="ca74c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca74c-104">SYNTAX</span></span>

### <span data-ttu-id="ca74c-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca74c-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca74c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca74c-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca74c-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca74c-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca74c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca74c-108">DESCRIPTION</span></span>
<span data-ttu-id="ca74c-109">Crie um encapsulamento SSH Kubectl para o painel do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ca74c-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="ca74c-110">O túnel SSH é configurado em um trabalho do PowerShell chamado Kubectl-Tunnel e pode ser encontrado em execução `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="ca74c-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="ca74c-111">O encapsulamento deve ser acessível via [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="ca74c-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="ca74c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca74c-112">EXAMPLES</span></span>

### <span data-ttu-id="ca74c-113">Iniciar um túnel SSH e abrir um navegador para o painel kubernetes</span><span class="sxs-lookup"><span data-stu-id="ca74c-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ca74c-114">OS</span><span class="sxs-lookup"><span data-stu-id="ca74c-114">PARAMETERS</span></span>

### <span data-ttu-id="ca74c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca74c-115">-DefaultProfile</span></span>
<span data-ttu-id="ca74c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca74c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca74c-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="ca74c-117">-DisableBrowser</span></span>
<span data-ttu-id="ca74c-118">Não abra abrir um navegador após estabelecer o encaminhamento de porta kubectl.</span><span class="sxs-lookup"><span data-stu-id="ca74c-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="ca74c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ca74c-119">-Id</span></span>
<span data-ttu-id="ca74c-120">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ca74c-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ca74c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca74c-121">-InputObject</span></span>
<span data-ttu-id="ca74c-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca74c-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ca74c-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="ca74c-123">-ListenPort</span></span>
<span data-ttu-id="ca74c-124">A porta de escuta do painel.</span><span class="sxs-lookup"><span data-stu-id="ca74c-124">The listening port for the dashboard.</span></span> <span data-ttu-id="ca74c-125">O valor padrão é 8003.</span><span class="sxs-lookup"><span data-stu-id="ca74c-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="ca74c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca74c-126">-Name</span></span>
<span data-ttu-id="ca74c-127">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ca74c-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ca74c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca74c-128">-PassThru</span></span>
<span data-ttu-id="ca74c-129">Cmdlet retorna o KubeTunnelJob se passado.</span><span class="sxs-lookup"><span data-stu-id="ca74c-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="ca74c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca74c-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca74c-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ca74c-131">Resource group name</span></span>

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

### <span data-ttu-id="ca74c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca74c-132">CommonParameters</span></span>
<span data-ttu-id="ca74c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca74c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca74c-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca74c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca74c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca74c-135">INPUTS</span></span>

### <span data-ttu-id="ca74c-136">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ca74c-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ca74c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ca74c-137">System.String</span></span>

## <span data-ttu-id="ca74c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca74c-138">OUTPUTS</span></span>

### <span data-ttu-id="ca74c-139">Microsoft. Azure. Commands. AKs. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="ca74c-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="ca74c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca74c-140">NOTES</span></span>

## <span data-ttu-id="ca74c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca74c-141">RELATED LINKS</span></span>
