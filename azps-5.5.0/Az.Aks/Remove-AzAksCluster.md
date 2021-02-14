---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116676"
---
# <span data-ttu-id="93a8f-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="93a8f-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="93a8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="93a8f-103">Excluir um cluster Desarnetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="93a8f-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="93a8f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93a8f-104">SYNTAX</span></span>

### <span data-ttu-id="93a8f-105">GroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93a8f-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93a8f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a8f-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93a8f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93a8f-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93a8f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="93a8f-108">DESCRIPTION</span></span>
<span data-ttu-id="93a8f-109">Excluir um cluster Desarnetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="93a8f-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="93a8f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="93a8f-110">EXAMPLES</span></span>

### <span data-ttu-id="93a8f-111">Excluir um cluster de RedeNetes gerenciado existente</span><span class="sxs-lookup"><span data-stu-id="93a8f-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="93a8f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93a8f-112">PARAMETERS</span></span>

### <span data-ttu-id="93a8f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93a8f-113">-AsJob</span></span>
<span data-ttu-id="93a8f-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="93a8f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93a8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a8f-115">-DefaultProfile</span></span>
<span data-ttu-id="93a8f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93a8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a8f-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="93a8f-117">-Force</span></span>
<span data-ttu-id="93a8f-118">Remover cluster de Redenetes gerenciadas sem aviso</span><span class="sxs-lookup"><span data-stu-id="93a8f-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="93a8f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="93a8f-119">-Id</span></span>
<span data-ttu-id="93a8f-120">ID de um cluster Desarnetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="93a8f-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93a8f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93a8f-121">-InputObject</span></span>
<span data-ttu-id="93a8f-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="93a8f-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="93a8f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="93a8f-123">-Name</span></span>
<span data-ttu-id="93a8f-124">Nome do cluster Desarnetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="93a8f-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93a8f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93a8f-125">-PassThru</span></span>
<span data-ttu-id="93a8f-126">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="93a8f-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="93a8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="93a8f-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="93a8f-128">Resource group name</span></span>

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

### <span data-ttu-id="93a8f-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="93a8f-129">-Confirm</span></span>
<span data-ttu-id="93a8f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93a8f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a8f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a8f-131">-WhatIf</span></span>
<span data-ttu-id="93a8f-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="93a8f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a8f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93a8f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a8f-134">CommonParameters</span></span>
<span data-ttu-id="93a8f-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a8f-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93a8f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a8f-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="93a8f-137">INPUTS</span></span>

### <span data-ttu-id="93a8f-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="93a8f-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="93a8f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="93a8f-139">System.String</span></span>

## <span data-ttu-id="93a8f-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="93a8f-140">OUTPUTS</span></span>

### <span data-ttu-id="93a8f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93a8f-141">System.Boolean</span></span>

## <span data-ttu-id="93a8f-142">Notas</span><span class="sxs-lookup"><span data-stu-id="93a8f-142">NOTES</span></span>

## <span data-ttu-id="93a8f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93a8f-143">RELATED LINKS</span></span>
