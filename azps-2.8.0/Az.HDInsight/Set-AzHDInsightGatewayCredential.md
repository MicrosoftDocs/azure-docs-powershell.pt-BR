---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 045b0db296a9c3bde4332ce755c055d1e8616738
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596331"
---
# <span data-ttu-id="1fda2-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="1fda2-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="1fda2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fda2-102">SYNOPSIS</span></span>
<span data-ttu-id="1fda2-103">Define as credenciais HTTP do gateway de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1fda2-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1fda2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fda2-104">SYNTAX</span></span>

### <span data-ttu-id="1fda2-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fda2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fda2-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fda2-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fda2-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fda2-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fda2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fda2-108">DESCRIPTION</span></span>
<span data-ttu-id="1fda2-109">O cmdlet **set-AzHDInsightGatewayCredential** define a credencial do gateway de um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1fda2-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1fda2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fda2-110">EXAMPLES</span></span>

### <span data-ttu-id="1fda2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fda2-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1fda2-112">Este comando define a credencial do gateway do cluster chamado seu-Hadoop-001 por parâmetro de nome definido.</span><span class="sxs-lookup"><span data-stu-id="1fda2-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="1fda2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1fda2-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1fda2-114">Este comando define a credencial do gateway do cluster chamado seu conjunto de parâmetros-Hadoop-001 by ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1fda2-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="1fda2-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1fda2-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="1fda2-116">Este comando define a credencial do gateway do cluster chamado seu-Hadoop-001 com o parâmetro InputObject definido.</span><span class="sxs-lookup"><span data-stu-id="1fda2-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="1fda2-117">OS</span><span class="sxs-lookup"><span data-stu-id="1fda2-117">PARAMETERS</span></span>

### <span data-ttu-id="1fda2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fda2-118">-AsJob</span></span>
<span data-ttu-id="1fda2-119">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1fda2-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1fda2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fda2-120">-DefaultProfile</span></span>
<span data-ttu-id="1fda2-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fda2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fda2-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1fda2-122">-HttpCredential</span></span>
<span data-ttu-id="1fda2-123">Obtém ou define o logon para o usuário do cluster.</span><span class="sxs-lookup"><span data-stu-id="1fda2-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fda2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fda2-124">-InputObject</span></span>
<span data-ttu-id="1fda2-125">Obtém ou define o objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1fda2-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fda2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fda2-126">-Name</span></span>
<span data-ttu-id="1fda2-127">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1fda2-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fda2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fda2-128">-ResourceGroupName</span></span>
<span data-ttu-id="1fda2-129">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fda2-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="1fda2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fda2-130">-ResourceId</span></span>
<span data-ttu-id="1fda2-131">Obtém ou define a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1fda2-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fda2-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1fda2-132">-Confirm</span></span>
<span data-ttu-id="1fda2-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fda2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fda2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fda2-134">-WhatIf</span></span>
<span data-ttu-id="1fda2-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fda2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fda2-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fda2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fda2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fda2-137">CommonParameters</span></span>
<span data-ttu-id="1fda2-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fda2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fda2-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fda2-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fda2-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fda2-140">INPUTS</span></span>

### <span data-ttu-id="1fda2-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1fda2-141">None</span></span>

## <span data-ttu-id="1fda2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fda2-142">OUTPUTS</span></span>

### <span data-ttu-id="1fda2-143">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="1fda2-143">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="1fda2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fda2-144">NOTES</span></span>

## <span data-ttu-id="1fda2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fda2-145">RELATED LINKS</span></span>
