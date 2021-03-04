---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 5d0cc543d5ec893ecb1f83b8fd62f25bcb32f5b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887257"
---
# <span data-ttu-id="67b45-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="67b45-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="67b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b45-102">SYNOPSIS</span></span>
<span data-ttu-id="67b45-103">Desabilite os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="67b45-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="67b45-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="67b45-104">SYNTAX</span></span>

### <span data-ttu-id="67b45-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67b45-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b45-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67b45-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b45-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="67b45-107">DESCRIPTION</span></span>
<span data-ttu-id="67b45-108">Desabilite os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="67b45-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="67b45-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67b45-109">EXAMPLES</span></span>

### <span data-ttu-id="67b45-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67b45-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="67b45-111">Desabilite os `HttpApplicationRouting` complementos `Monitoring` , , e para `AzurePolicy` `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="67b45-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="67b45-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="67b45-112">PARAMETERS</span></span>

### <span data-ttu-id="67b45-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67b45-113">-ClusterName</span></span>
<span data-ttu-id="67b45-114">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="67b45-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="67b45-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="67b45-115">-ClusterObject</span></span>
<span data-ttu-id="67b45-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="67b45-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="67b45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b45-117">-DefaultProfile</span></span>
<span data-ttu-id="67b45-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67b45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b45-119">-Name</span><span class="sxs-lookup"><span data-stu-id="67b45-119">-Name</span></span>
<span data-ttu-id="67b45-120">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="67b45-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="67b45-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b45-121">-ResourceGroupName</span></span>
<span data-ttu-id="67b45-122">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="67b45-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="67b45-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67b45-123">-Confirm</span></span>
<span data-ttu-id="67b45-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67b45-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b45-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b45-125">-WhatIf</span></span>
<span data-ttu-id="67b45-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67b45-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67b45-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67b45-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b45-128">CommonParameters</span></span>
<span data-ttu-id="67b45-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b45-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67b45-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b45-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67b45-131">INPUTS</span></span>

### <span data-ttu-id="67b45-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="67b45-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="67b45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="67b45-133">System.String</span></span>

## <span data-ttu-id="67b45-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="67b45-134">OUTPUTS</span></span>

### <span data-ttu-id="67b45-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="67b45-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="67b45-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="67b45-136">NOTES</span></span>

## <span data-ttu-id="67b45-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67b45-137">RELATED LINKS</span></span>
