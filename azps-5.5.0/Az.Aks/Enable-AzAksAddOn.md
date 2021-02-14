---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 40fb9f328f0f838f5d76de6de5509c74b0002768
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116694"
---
# <span data-ttu-id="62bd8-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="62bd8-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="62bd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="62bd8-103">Habilita os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="62bd8-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="62bd8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62bd8-104">SYNTAX</span></span>

### <span data-ttu-id="62bd8-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62bd8-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62bd8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62bd8-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62bd8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="62bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="62bd8-108">Habilita os complementos para aks.</span><span class="sxs-lookup"><span data-stu-id="62bd8-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="62bd8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62bd8-109">EXAMPLES</span></span>

### <span data-ttu-id="62bd8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62bd8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="62bd8-111">Habilita os `HttpApplicationRouting` `Monitoring` complementos `AzurePolicy` e as `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="62bd8-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="62bd8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62bd8-112">PARAMETERS</span></span>

### <span data-ttu-id="62bd8-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="62bd8-113">-ClusterName</span></span>
<span data-ttu-id="62bd8-114">Nome de cluster gerenciado da Rede Desavenda.</span><span class="sxs-lookup"><span data-stu-id="62bd8-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="62bd8-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="62bd8-115">-ClusterObject</span></span>
<span data-ttu-id="62bd8-116">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="62bd8-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="62bd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bd8-117">-DefaultProfile</span></span>
<span data-ttu-id="62bd8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62bd8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bd8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="62bd8-119">-Name</span></span>
<span data-ttu-id="62bd8-120">Nome de cluster gerenciado da Rede Desavenda.</span><span class="sxs-lookup"><span data-stu-id="62bd8-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="62bd8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bd8-121">-ResourceGroupName</span></span>
<span data-ttu-id="62bd8-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62bd8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="62bd8-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="62bd8-123">-SubnetName</span></span>
<span data-ttu-id="62bd8-124">Nome da sub-rede do VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="62bd8-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="62bd8-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="62bd8-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="62bd8-126">ID do recurso do espaço de trabalho de Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="62bd8-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="62bd8-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62bd8-127">-Confirm</span></span>
<span data-ttu-id="62bd8-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62bd8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bd8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bd8-129">-WhatIf</span></span>
<span data-ttu-id="62bd8-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62bd8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bd8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62bd8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bd8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bd8-132">CommonParameters</span></span>
<span data-ttu-id="62bd8-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bd8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bd8-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62bd8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bd8-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="62bd8-135">INPUTS</span></span>

### <span data-ttu-id="62bd8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="62bd8-136">System.String</span></span>

### <span data-ttu-id="62bd8-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="62bd8-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="62bd8-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="62bd8-138">OUTPUTS</span></span>

### <span data-ttu-id="62bd8-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="62bd8-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="62bd8-140">Notas</span><span class="sxs-lookup"><span data-stu-id="62bd8-140">NOTES</span></span>

## <span data-ttu-id="62bd8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62bd8-141">RELATED LINKS</span></span>
