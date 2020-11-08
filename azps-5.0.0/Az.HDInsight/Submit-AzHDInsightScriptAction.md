---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: dfae83e6bd540a83475f02ed95382bebff2ec7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117830"
---
# <span data-ttu-id="8e6a4-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="8e6a4-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="8e6a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6a4-103">Envia uma nova ação de script para um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8e6a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e6a4-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e6a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e6a4-106">O cmdlet **Submit-AzHDInsightScriptAction** envia uma nova ação de script para um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="8e6a4-107">Use o *PersistOnSuccess* para executar a ação do script cada vez que o cluster for ampliado, desde que a ação do script inicialmente seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="8e6a4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e6a4-108">EXAMPLES</span></span>

### <span data-ttu-id="8e6a4-109">Exemplo 1: Enviar uma nova ação de script para um cluster do HDInsight em execução</span><span class="sxs-lookup"><span data-stu-id="8e6a4-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="8e6a4-110">Esse comando envia uma ação de script para um cluster HDInsight em execução.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="8e6a4-111">OS</span><span class="sxs-lookup"><span data-stu-id="8e6a4-111">PARAMETERS</span></span>

### <span data-ttu-id="8e6a4-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="8e6a4-112">-ApplicationName</span></span>
<span data-ttu-id="8e6a4-113">Especifica o nome do aplicativo para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="8e6a4-114">Quando *ApplicationName* é especificado, *PersistOnSuccess* deve ser definido como false, os nós devem conter somente edgenode, e a contagem de ação do script deve ser igual a 1.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="8e6a4-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e6a4-115">-ClusterName</span></span>
<span data-ttu-id="8e6a4-116">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8e6a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6a4-117">-DefaultProfile</span></span>
<span data-ttu-id="8e6a4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8e6a4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e6a4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e6a4-119">-Name</span></span>
<span data-ttu-id="8e6a4-120">Especifica o nome da ação do script.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="8e6a4-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="8e6a4-121">-NodeTypes</span></span>
<span data-ttu-id="8e6a4-122">Especifica os tipos de nós para executar a ação de script.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="8e6a4-123">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e6a4-123">-Parameters</span></span>
<span data-ttu-id="8e6a4-124">Especifica os parâmetros para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="8e6a4-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="8e6a4-125">-PersistOnSuccess</span></span>
<span data-ttu-id="8e6a4-126">Indica que a ação de script deve ser executada toda vez que o cluster é ampliado.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="8e6a4-127">Esse parâmetro de opção será ignorado se a ação do script falhar inicialmente.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="8e6a4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e6a4-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e6a4-129">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8e6a4-130">-URI</span><span class="sxs-lookup"><span data-stu-id="8e6a4-130">-Uri</span></span>
<span data-ttu-id="8e6a4-131">Especifica o URI público para a ação do script (um script do PowerShell ou de bash).</span><span class="sxs-lookup"><span data-stu-id="8e6a4-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="8e6a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6a4-132">CommonParameters</span></span>
<span data-ttu-id="8e6a4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e6a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6a4-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e6a4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6a4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e6a4-135">INPUTS</span></span>

### <span data-ttu-id="8e6a4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e6a4-136">System.String</span></span>

### <span data-ttu-id="8e6a4-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="8e6a4-137">System.Uri</span></span>

### <span data-ttu-id="8e6a4-138">Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="8e6a4-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="8e6a4-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e6a4-139">OUTPUTS</span></span>

### <span data-ttu-id="8e6a4-140">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="8e6a4-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="8e6a4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e6a4-141">NOTES</span></span>

## <span data-ttu-id="8e6a4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e6a4-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e6a4-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="8e6a4-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


