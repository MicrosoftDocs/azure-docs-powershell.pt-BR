---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887255"
---
# <span data-ttu-id="77989-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="77989-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="77989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77989-102">SYNOPSIS</span></span>
<span data-ttu-id="77989-103">Habilita os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="77989-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="77989-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77989-104">SYNTAX</span></span>

### <span data-ttu-id="77989-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="77989-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77989-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77989-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77989-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77989-107">DESCRIPTION</span></span>
<span data-ttu-id="77989-108">Habilita os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="77989-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="77989-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77989-109">EXAMPLES</span></span>

### <span data-ttu-id="77989-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77989-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="77989-111">Habilita os `HttpApplicationRouting` complementos `Monitoring` , , e para `AzurePolicy` `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="77989-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="77989-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77989-112">PARAMETERS</span></span>

### <span data-ttu-id="77989-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="77989-113">-ClusterName</span></span>
<span data-ttu-id="77989-114">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="77989-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="77989-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="77989-115">-ClusterObject</span></span>
<span data-ttu-id="77989-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="77989-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="77989-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77989-117">-DefaultProfile</span></span>
<span data-ttu-id="77989-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77989-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77989-119">-Name</span><span class="sxs-lookup"><span data-stu-id="77989-119">-Name</span></span>
<span data-ttu-id="77989-120">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="77989-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="77989-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77989-121">-ResourceGroupName</span></span>
<span data-ttu-id="77989-122">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="77989-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="77989-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="77989-123">-SubnetName</span></span>
<span data-ttu-id="77989-124">Nome da sub-rede de VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="77989-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="77989-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="77989-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="77989-126">ID de recurso do espaço de trabalho do Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="77989-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="77989-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77989-127">-Confirm</span></span>
<span data-ttu-id="77989-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77989-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77989-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77989-129">-WhatIf</span></span>
<span data-ttu-id="77989-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77989-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77989-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77989-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77989-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77989-132">CommonParameters</span></span>
<span data-ttu-id="77989-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77989-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77989-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77989-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77989-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77989-135">INPUTS</span></span>

### <span data-ttu-id="77989-136">System.String</span><span class="sxs-lookup"><span data-stu-id="77989-136">System.String</span></span>

### <span data-ttu-id="77989-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="77989-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="77989-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77989-138">OUTPUTS</span></span>

### <span data-ttu-id="77989-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="77989-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="77989-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="77989-140">NOTES</span></span>

## <span data-ttu-id="77989-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77989-141">RELATED LINKS</span></span>
