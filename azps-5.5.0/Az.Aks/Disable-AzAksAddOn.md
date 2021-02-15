---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 616695e60d945e545cfbb8c1b2fb7ba81ae9caa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114317"
---
# <span data-ttu-id="23df7-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="23df7-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="23df7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23df7-102">SYNOPSIS</span></span>
<span data-ttu-id="23df7-103">Desabilite os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="23df7-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="23df7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23df7-104">SYNTAX</span></span>

### <span data-ttu-id="23df7-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23df7-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23df7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23df7-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23df7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="23df7-107">DESCRIPTION</span></span>
<span data-ttu-id="23df7-108">Desabilite os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="23df7-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="23df7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23df7-109">EXAMPLES</span></span>

### <span data-ttu-id="23df7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23df7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="23df7-111">Desabilite os `HttpApplicationRouting` `Monitoring` complementos, `AzurePolicy` e para `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="23df7-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="23df7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23df7-112">PARAMETERS</span></span>

### <span data-ttu-id="23df7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="23df7-113">-ClusterName</span></span>
<span data-ttu-id="23df7-114">Nome de cluster gerenciado por RedeNetes.</span><span class="sxs-lookup"><span data-stu-id="23df7-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="23df7-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="23df7-115">-ClusterObject</span></span>
<span data-ttu-id="23df7-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="23df7-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="23df7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23df7-117">-DefaultProfile</span></span>
<span data-ttu-id="23df7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23df7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23df7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="23df7-119">-Name</span></span>
<span data-ttu-id="23df7-120">Nome de cluster gerenciado por RedeNetes.</span><span class="sxs-lookup"><span data-stu-id="23df7-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="23df7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23df7-121">-ResourceGroupName</span></span>
<span data-ttu-id="23df7-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23df7-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="23df7-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="23df7-123">-Confirm</span></span>
<span data-ttu-id="23df7-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23df7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23df7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23df7-125">-WhatIf</span></span>
<span data-ttu-id="23df7-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="23df7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23df7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23df7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23df7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23df7-128">CommonParameters</span></span>
<span data-ttu-id="23df7-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23df7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23df7-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23df7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23df7-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="23df7-131">INPUTS</span></span>

### <span data-ttu-id="23df7-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="23df7-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="23df7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="23df7-133">System.String</span></span>

## <span data-ttu-id="23df7-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="23df7-134">OUTPUTS</span></span>

### <span data-ttu-id="23df7-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="23df7-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="23df7-136">Notas</span><span class="sxs-lookup"><span data-stu-id="23df7-136">NOTES</span></span>

## <span data-ttu-id="23df7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23df7-137">RELATED LINKS</span></span>
