---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429038"
---
# <span data-ttu-id="301b1-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="301b1-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="301b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="301b1-102">SYNOPSIS</span></span>
<span data-ttu-id="301b1-103">Habilite os Complementos para AKs.</span><span class="sxs-lookup"><span data-stu-id="301b1-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="301b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="301b1-104">SYNTAX</span></span>

### <span data-ttu-id="301b1-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="301b1-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="301b1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="301b1-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301b1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="301b1-107">DESCRIPTION</span></span>
<span data-ttu-id="301b1-108">Habilite os Complementos para AKs.</span><span class="sxs-lookup"><span data-stu-id="301b1-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="301b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="301b1-109">EXAMPLES</span></span>

### <span data-ttu-id="301b1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="301b1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="301b1-111">Habilite os complementos `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` e `KubeDashboard` para AKs.</span><span class="sxs-lookup"><span data-stu-id="301b1-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="301b1-112">OS</span><span class="sxs-lookup"><span data-stu-id="301b1-112">PARAMETERS</span></span>

### <span data-ttu-id="301b1-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="301b1-113">-ClusterName</span></span>
<span data-ttu-id="301b1-114">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="301b1-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="301b1-115">-ClusterObject</span></span>
<span data-ttu-id="301b1-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="301b1-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301b1-117">-DefaultProfile</span></span>
<span data-ttu-id="301b1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="301b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301b1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="301b1-119">-Name</span></span>
<span data-ttu-id="301b1-120">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="301b1-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="301b1-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="301b1-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="301b1-123">-SubnetName</span></span>
<span data-ttu-id="301b1-124">Nome da sub-rede VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="301b1-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="301b1-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="301b1-126">ID do recurso do espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="301b1-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301b1-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="301b1-127">-Confirm</span></span>
<span data-ttu-id="301b1-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="301b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301b1-129">-WhatIf</span></span>
<span data-ttu-id="301b1-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="301b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301b1-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="301b1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301b1-132">CommonParameters</span></span>
<span data-ttu-id="301b1-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301b1-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="301b1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301b1-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="301b1-135">INPUTS</span></span>

### <span data-ttu-id="301b1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="301b1-136">System.String</span></span>

### <span data-ttu-id="301b1-137">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="301b1-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="301b1-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="301b1-138">OUTPUTS</span></span>

### <span data-ttu-id="301b1-139">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="301b1-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="301b1-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="301b1-140">NOTES</span></span>

## <span data-ttu-id="301b1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="301b1-141">RELATED LINKS</span></span>
