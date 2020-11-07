---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947740"
---
# <span data-ttu-id="a9662-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="a9662-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="a9662-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9662-102">SYNOPSIS</span></span>
<span data-ttu-id="a9662-103">Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a9662-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="a9662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9662-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9662-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9662-105">DESCRIPTION</span></span>
<span data-ttu-id="a9662-106">O cmdlet **Get-AzHDInsightScriptActionHistory** Obtém o histórico da ação de script de um cluster do Azure HDInsight e o lista em ordem cronológica inversa, ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a9662-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="a9662-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9662-107">EXAMPLES</span></span>

### <span data-ttu-id="a9662-108">Exemplo 1: obter o histórico de execuções de ações de script para um cluster</span><span class="sxs-lookup"><span data-stu-id="a9662-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a9662-109">Esse comando obtém o histórico de ações de script para o cluster seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a9662-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="a9662-110">OS</span><span class="sxs-lookup"><span data-stu-id="a9662-110">PARAMETERS</span></span>

### <span data-ttu-id="a9662-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a9662-111">-ClusterName</span></span>
<span data-ttu-id="a9662-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a9662-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a9662-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9662-113">-DefaultProfile</span></span>
<span data-ttu-id="a9662-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9662-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9662-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9662-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9662-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9662-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a9662-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="a9662-117">-ScriptExecutionId</span></span>
<span data-ttu-id="a9662-118">Especifica a ID de execução da ação de script executada.</span><span class="sxs-lookup"><span data-stu-id="a9662-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9662-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9662-119">CommonParameters</span></span>
<span data-ttu-id="a9662-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9662-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9662-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9662-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9662-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9662-122">INPUTS</span></span>

### <span data-ttu-id="a9662-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9662-123">None</span></span>

## <span data-ttu-id="a9662-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9662-124">OUTPUTS</span></span>

### <span data-ttu-id="a9662-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="a9662-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="a9662-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9662-126">NOTES</span></span>

## <span data-ttu-id="a9662-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9662-127">RELATED LINKS</span></span>
