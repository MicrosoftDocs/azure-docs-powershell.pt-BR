---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 884741f6543dee05ed8236385071ad345321413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430255"
---
# <span data-ttu-id="575cf-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="575cf-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="575cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="575cf-102">SYNOPSIS</span></span>
<span data-ttu-id="575cf-103">Envia uma nova ação de script para um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="575cf-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="575cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="575cf-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="575cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="575cf-105">DESCRIPTION</span></span>
<span data-ttu-id="575cf-106">O cmdlet **Submit-AzureRmHDInsightScriptAction** envia uma nova ação de script para um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="575cf-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="575cf-107">Use o *PersistOnSuccess* para executar a ação do script cada vez que o cluster for ampliado, desde que a ação do script inicialmente seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="575cf-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="575cf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="575cf-108">EXAMPLES</span></span>

### <span data-ttu-id="575cf-109">Exemplo 1: Enviar uma nova ação de script para um cluster do HDInsight em execução</span><span class="sxs-lookup"><span data-stu-id="575cf-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="575cf-110">Esse comando envia uma ação de script para um cluster HDInsight em execução.</span><span class="sxs-lookup"><span data-stu-id="575cf-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="575cf-111">OS</span><span class="sxs-lookup"><span data-stu-id="575cf-111">PARAMETERS</span></span>

### <span data-ttu-id="575cf-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="575cf-112">-ApplicationName</span></span>
<span data-ttu-id="575cf-113">Especifica o nome do aplicativo para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="575cf-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="575cf-114">Quando *ApplicationName* é especificado, *PersistOnSuccess* deve ser definido como false, os nós devem conter somente edgenode, e a contagem de ação do script deve ser igual a 1.</span><span class="sxs-lookup"><span data-stu-id="575cf-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="575cf-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="575cf-115">-ClusterName</span></span>
<span data-ttu-id="575cf-116">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="575cf-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="575cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575cf-117">-DefaultProfile</span></span>
<span data-ttu-id="575cf-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="575cf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575cf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="575cf-119">-Name</span></span>
<span data-ttu-id="575cf-120">Especifica o nome da ação do script.</span><span class="sxs-lookup"><span data-stu-id="575cf-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="575cf-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="575cf-121">-NodeTypes</span></span>
<span data-ttu-id="575cf-122">Especifica os tipos de nós para executar a ação de script.</span><span class="sxs-lookup"><span data-stu-id="575cf-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="575cf-123">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="575cf-123">-Parameters</span></span>
<span data-ttu-id="575cf-124">Especifica os parâmetros para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="575cf-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="575cf-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="575cf-125">-PersistOnSuccess</span></span>
<span data-ttu-id="575cf-126">Indica que a ação de script deve ser executada toda vez que o cluster é ampliado.</span><span class="sxs-lookup"><span data-stu-id="575cf-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="575cf-127">Esse parâmetro de opção será ignorado se a ação do script falhar inicialmente.</span><span class="sxs-lookup"><span data-stu-id="575cf-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="575cf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575cf-128">-ResourceGroupName</span></span>
<span data-ttu-id="575cf-129">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="575cf-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="575cf-130">-URI</span><span class="sxs-lookup"><span data-stu-id="575cf-130">-Uri</span></span>
<span data-ttu-id="575cf-131">Especifica o URI público para a ação do script (um script do PowerShell ou de bash).</span><span class="sxs-lookup"><span data-stu-id="575cf-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="575cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575cf-132">CommonParameters</span></span>
<span data-ttu-id="575cf-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575cf-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575cf-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="575cf-135">INPUTS</span></span>

### <span data-ttu-id="575cf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="575cf-136">System.String</span></span>

### <span data-ttu-id="575cf-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="575cf-137">System.Uri</span></span>

### <span data-ttu-id="575cf-138">Microsoft. Azure. Commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="575cf-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="575cf-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="575cf-139">OUTPUTS</span></span>

### <span data-ttu-id="575cf-140">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="575cf-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="575cf-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="575cf-141">NOTES</span></span>

## <span data-ttu-id="575cf-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="575cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="575cf-143">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="575cf-143">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


