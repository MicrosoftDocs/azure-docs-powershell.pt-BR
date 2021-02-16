---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: 3cbd73075445bdcf65efafb266476c522dc4b1ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113181"
---
# <span data-ttu-id="1445e-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="1445e-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="1445e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1445e-102">SYNOPSIS</span></span>
<span data-ttu-id="1445e-103">Envia uma nova ação de script para um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="1445e-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1445e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1445e-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1445e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1445e-105">DESCRIPTION</span></span>
<span data-ttu-id="1445e-106">O cmdlet **Submit-AzHDInsightScriptAction** envia uma nova ação de script para um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="1445e-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="1445e-107">Use *PersistOnSuccess* para executar a ação de script sempre que o cluster for dimensionado, desde que a ação de script seja bem-sucedida inicialmente.</span><span class="sxs-lookup"><span data-stu-id="1445e-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="1445e-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1445e-108">EXAMPLES</span></span>

### <span data-ttu-id="1445e-109">Exemplo 1: Enviar uma nova ação de script para um cluster HDInsight em execução</span><span class="sxs-lookup"><span data-stu-id="1445e-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="1445e-110">Esse comando envia uma ação de script para um cluster HDInsight em execução.</span><span class="sxs-lookup"><span data-stu-id="1445e-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="1445e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1445e-111">PARAMETERS</span></span>

### <span data-ttu-id="1445e-112">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="1445e-112">-ApplicationName</span></span>
<span data-ttu-id="1445e-113">Especifica o nome do aplicativo para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="1445e-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="1445e-114">Quando *ApplicationName* é especificado, *PersistOnSuccess* deve ser definido como False, nós devem conter apenas edgenode e a contagem de ações de script deve ser igual a 1.</span><span class="sxs-lookup"><span data-stu-id="1445e-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1445e-115">-ClusterName</span></span>
<span data-ttu-id="1445e-116">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="1445e-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1445e-117">-DefaultProfile</span></span>
<span data-ttu-id="1445e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1445e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1445e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1445e-119">-Name</span></span>
<span data-ttu-id="1445e-120">Especifica o nome da ação de script.</span><span class="sxs-lookup"><span data-stu-id="1445e-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="1445e-121">-NodeTypes</span></span>
<span data-ttu-id="1445e-122">Especifica os tipos de nó nos quais executar a ação de script.</span><span class="sxs-lookup"><span data-stu-id="1445e-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-123">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1445e-123">-Parameters</span></span>
<span data-ttu-id="1445e-124">Especifica os parâmetros da ação de script.</span><span class="sxs-lookup"><span data-stu-id="1445e-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="1445e-125">-PersistOnSuccess</span></span>
<span data-ttu-id="1445e-126">Indica que a ação de script deve ser executado sempre que o cluster for dimensionado.</span><span class="sxs-lookup"><span data-stu-id="1445e-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="1445e-127">Esse parâmetro de opção será ignorado se a ação de script falhar inicialmente.</span><span class="sxs-lookup"><span data-stu-id="1445e-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1445e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1445e-129">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1445e-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1445e-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="1445e-130">-Uri</span></span>
<span data-ttu-id="1445e-131">Especifica o URI público para a ação de script (um script do PowerShell ou Bash).</span><span class="sxs-lookup"><span data-stu-id="1445e-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1445e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1445e-132">CommonParameters</span></span>
<span data-ttu-id="1445e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1445e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1445e-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1445e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1445e-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1445e-135">INPUTS</span></span>

### <span data-ttu-id="1445e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1445e-136">System.String</span></span>

### <span data-ttu-id="1445e-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="1445e-137">System.Uri</span></span>

### <span data-ttu-id="1445e-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span><span class="sxs-lookup"><span data-stu-id="1445e-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="1445e-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="1445e-139">OUTPUTS</span></span>

### <span data-ttu-id="1445e-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="1445e-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="1445e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="1445e-141">NOTES</span></span>

## <span data-ttu-id="1445e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1445e-142">RELATED LINKS</span></span>

[<span data-ttu-id="1445e-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="1445e-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


