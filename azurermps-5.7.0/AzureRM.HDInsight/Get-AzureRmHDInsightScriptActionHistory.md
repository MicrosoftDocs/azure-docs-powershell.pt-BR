---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426702"
---
# <span data-ttu-id="b358f-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="b358f-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="b358f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b358f-102">SYNOPSIS</span></span>
<span data-ttu-id="b358f-103">Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b358f-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b358f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b358f-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b358f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b358f-105">DESCRIPTION</span></span>
<span data-ttu-id="b358f-106">O cmdlet **Get-AzureRmHDInsightScriptActionHistory** Obtém o histórico da ação de script de um cluster do Azure HDInsight e o lista em ordem cronológica inversa, ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b358f-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="b358f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b358f-107">EXAMPLES</span></span>

### <span data-ttu-id="b358f-108">Exemplo 1: obter o histórico de execuções de ações de script para um cluster</span><span class="sxs-lookup"><span data-stu-id="b358f-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b358f-109">Esse comando obtém o histórico de ações de script para o cluster seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b358f-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="b358f-110">OS</span><span class="sxs-lookup"><span data-stu-id="b358f-110">PARAMETERS</span></span>

### <span data-ttu-id="b358f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b358f-111">-ClusterName</span></span>
<span data-ttu-id="b358f-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="b358f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b358f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b358f-113">-DefaultProfile</span></span>
<span data-ttu-id="b358f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b358f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b358f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b358f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b358f-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b358f-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b358f-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b358f-117">-ScriptExecutionId</span></span>
<span data-ttu-id="b358f-118">Especifica a ID de execução da ação de script executada.</span><span class="sxs-lookup"><span data-stu-id="b358f-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b358f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b358f-119">CommonParameters</span></span>
<span data-ttu-id="b358f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b358f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b358f-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b358f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b358f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b358f-122">INPUTS</span></span>

### <span data-ttu-id="b358f-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b358f-123">None</span></span>
<span data-ttu-id="b358f-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b358f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b358f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b358f-125">OUTPUTS</span></span>

### <span data-ttu-id="b358f-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="b358f-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="b358f-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b358f-127">NOTES</span></span>

## <span data-ttu-id="b358f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b358f-128">RELATED LINKS</span></span>
