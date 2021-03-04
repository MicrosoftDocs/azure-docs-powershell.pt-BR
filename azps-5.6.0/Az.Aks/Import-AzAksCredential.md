---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: 06ea31f48dbe3b1d5a103598f7f16953bfc449ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887245"
---
# <span data-ttu-id="c77cf-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="c77cf-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="c77cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c77cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c77cf-103">Importar e mesclar config do Kubectl para um Cluster Kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c77cf-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c77cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c77cf-104">SYNTAX</span></span>

### <span data-ttu-id="c77cf-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c77cf-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c77cf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c77cf-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c77cf-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c77cf-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c77cf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c77cf-108">DESCRIPTION</span></span>
<span data-ttu-id="c77cf-109">Importar e mesclar config do Kubectl para um Cluster Kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c77cf-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="c77cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c77cf-110">EXAMPLES</span></span>

### <span data-ttu-id="c77cf-111">Importar e mesclar config kubectl</span><span class="sxs-lookup"><span data-stu-id="c77cf-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c77cf-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c77cf-112">PARAMETERS</span></span>

### <span data-ttu-id="c77cf-113">-Admin</span><span class="sxs-lookup"><span data-stu-id="c77cf-113">-Admin</span></span>
<span data-ttu-id="c77cf-114">Obter a configuração kubectl 'clusterAdmin' em vez do padrão 'clusterUser'.</span><span class="sxs-lookup"><span data-stu-id="c77cf-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="c77cf-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="c77cf-115">-ConfigPath</span></span>
<span data-ttu-id="c77cf-116">Um arquivo de configuração kubectl para criar ou atualizar.</span><span class="sxs-lookup"><span data-stu-id="c77cf-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="c77cf-117">Use '-' para imprimir YAML para stdout.</span><span class="sxs-lookup"><span data-stu-id="c77cf-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="c77cf-118">Padrão: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="c77cf-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="c77cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77cf-119">-DefaultProfile</span></span>
<span data-ttu-id="c77cf-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c77cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c77cf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c77cf-121">-Force</span></span>
<span data-ttu-id="c77cf-122">Importar Kubernetes config mesmo que seja o padrão</span><span class="sxs-lookup"><span data-stu-id="c77cf-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="c77cf-123">-Id</span><span class="sxs-lookup"><span data-stu-id="c77cf-123">-Id</span></span>
<span data-ttu-id="c77cf-124">ID de um cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="c77cf-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c77cf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c77cf-125">-InputObject</span></span>
<span data-ttu-id="c77cf-126">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c77cf-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c77cf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c77cf-127">-Name</span></span>
<span data-ttu-id="c77cf-128">Nome do cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="c77cf-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c77cf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c77cf-129">-PassThru</span></span>
<span data-ttu-id="c77cf-130">Retorna true se a importação for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="c77cf-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="c77cf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c77cf-131">-ResourceGroupName</span></span>
<span data-ttu-id="c77cf-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c77cf-132">Resource group name</span></span>

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

### <span data-ttu-id="c77cf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c77cf-133">-Confirm</span></span>
<span data-ttu-id="c77cf-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c77cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c77cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c77cf-135">-WhatIf</span></span>
<span data-ttu-id="c77cf-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c77cf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c77cf-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c77cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c77cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77cf-138">CommonParameters</span></span>
<span data-ttu-id="c77cf-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c77cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77cf-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c77cf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77cf-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c77cf-141">INPUTS</span></span>

### <span data-ttu-id="c77cf-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c77cf-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c77cf-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c77cf-143">System.String</span></span>

## <span data-ttu-id="c77cf-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c77cf-144">OUTPUTS</span></span>

### <span data-ttu-id="c77cf-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c77cf-145">System.String</span></span>

## <span data-ttu-id="c77cf-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="c77cf-146">NOTES</span></span>

## <span data-ttu-id="c77cf-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c77cf-147">RELATED LINKS</span></span>
