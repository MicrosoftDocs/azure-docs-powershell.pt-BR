---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 2a66333f5372308c87462f5ef9b2f7f5bfa8dd79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770805"
---
# <span data-ttu-id="dd074-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="dd074-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="dd074-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd074-102">SYNOPSIS</span></span>
<span data-ttu-id="dd074-103">Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dd074-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="dd074-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd074-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd074-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd074-105">DESCRIPTION</span></span>
<span data-ttu-id="dd074-106">O cmdlet **Get-AzHDInsightScriptActionHistory** Obtém o histórico da ação de script de um cluster do Azure HDInsight e o lista em ordem cronológica inversa, ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dd074-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="dd074-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd074-107">EXAMPLES</span></span>

### <span data-ttu-id="dd074-108">Exemplo 1: obter o histórico de execuções de ações de script para um cluster</span><span class="sxs-lookup"><span data-stu-id="dd074-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="dd074-109">Esse comando obtém o histórico de ações de script para o cluster seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="dd074-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="dd074-110">OS</span><span class="sxs-lookup"><span data-stu-id="dd074-110">PARAMETERS</span></span>

### <span data-ttu-id="dd074-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dd074-111">-ClusterName</span></span>
<span data-ttu-id="dd074-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="dd074-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="dd074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd074-113">-DefaultProfile</span></span>
<span data-ttu-id="dd074-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dd074-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd074-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd074-115">-ResourceGroupName</span></span>
<span data-ttu-id="dd074-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd074-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dd074-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="dd074-117">-ScriptExecutionId</span></span>
<span data-ttu-id="dd074-118">Especifica a ID de execução da ação de script executada.</span><span class="sxs-lookup"><span data-stu-id="dd074-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="dd074-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd074-119">CommonParameters</span></span>
<span data-ttu-id="dd074-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd074-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd074-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd074-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd074-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd074-122">INPUTS</span></span>

### <span data-ttu-id="dd074-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dd074-123">None</span></span>

## <span data-ttu-id="dd074-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd074-124">OUTPUTS</span></span>

### <span data-ttu-id="dd074-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="dd074-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="dd074-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd074-126">NOTES</span></span>

## <span data-ttu-id="dd074-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd074-127">RELATED LINKS</span></span>
