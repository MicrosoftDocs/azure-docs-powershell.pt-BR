---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948031"
---
# <span data-ttu-id="9e1e8-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="9e1e8-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="9e1e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e1e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1e8-103">Desabilite os Complementos para AKs.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="9e1e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e1e8-104">SYNTAX</span></span>

### <span data-ttu-id="9e1e8-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e1e8-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e1e8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e1e8-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e1e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e1e8-107">DESCRIPTION</span></span>
<span data-ttu-id="9e1e8-108">Desabilite os Complementos para AKs.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="9e1e8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e1e8-109">EXAMPLES</span></span>

### <span data-ttu-id="9e1e8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9e1e8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="9e1e8-111">Desabilite os complementos `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` e `KubeDashboard` para AKs.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="9e1e8-112">OS</span><span class="sxs-lookup"><span data-stu-id="9e1e8-112">PARAMETERS</span></span>

### <span data-ttu-id="9e1e8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9e1e8-113">-ClusterName</span></span>
<span data-ttu-id="9e1e8-114">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="9e1e8-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="9e1e8-115">-ClusterObject</span></span>
<span data-ttu-id="9e1e8-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e1e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1e8-117">-DefaultProfile</span></span>
<span data-ttu-id="9e1e8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e1e8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e1e8-119">-Name</span></span>
<span data-ttu-id="9e1e8-120">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="9e1e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e1e8-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e1e8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e1e8-123">-Confirm</span></span>
<span data-ttu-id="9e1e8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e1e8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e1e8-125">-WhatIf</span></span>
<span data-ttu-id="9e1e8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e1e8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e1e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1e8-128">CommonParameters</span></span>
<span data-ttu-id="9e1e8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1e8-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e1e8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1e8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e1e8-131">INPUTS</span></span>

### <span data-ttu-id="9e1e8-132">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9e1e8-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="9e1e8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9e1e8-133">System.String</span></span>

## <span data-ttu-id="9e1e8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e1e8-134">OUTPUTS</span></span>

### <span data-ttu-id="9e1e8-135">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9e1e8-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="9e1e8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e1e8-136">NOTES</span></span>

## <span data-ttu-id="9e1e8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e1e8-137">RELATED LINKS</span></span>
