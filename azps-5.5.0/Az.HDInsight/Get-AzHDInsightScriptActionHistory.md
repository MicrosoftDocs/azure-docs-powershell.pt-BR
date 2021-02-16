---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 0424578473aedb60071e3389e7aaff2b84848f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118466"
---
# <span data-ttu-id="9bcd4-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="9bcd4-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="9bcd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcd4-103">Obtém o histórico de ações de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="9bcd4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bcd4-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bcd4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bcd4-105">DESCRIPTION</span></span>
<span data-ttu-id="9bcd4-106">O cmdlet **Get-AzHDInsightScriptActionHistory** obtém o histórico de ações de script de um cluster HDInsight do Azure e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="9bcd4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bcd4-107">EXAMPLES</span></span>

### <span data-ttu-id="9bcd4-108">Exemplo 1: Obter o histórico de execução de ações de script para um cluster</span><span class="sxs-lookup"><span data-stu-id="9bcd4-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="9bcd4-109">Esse comando obtém o histórico de ações de script para o cluster seu-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="9bcd4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bcd4-110">PARAMETERS</span></span>

### <span data-ttu-id="9bcd4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9bcd4-111">-ClusterName</span></span>
<span data-ttu-id="9bcd4-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9bcd4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcd4-113">-DefaultProfile</span></span>
<span data-ttu-id="9bcd4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9bcd4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bcd4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcd4-115">-ResourceGroupName</span></span>
<span data-ttu-id="9bcd4-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9bcd4-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="9bcd4-117">-ScriptExecutionId</span></span>
<span data-ttu-id="9bcd4-118">Especifica a ID de execução da ação de script executada.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="9bcd4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcd4-119">CommonParameters</span></span>
<span data-ttu-id="9bcd4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcd4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcd4-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bcd4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcd4-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bcd4-122">INPUTS</span></span>

### <span data-ttu-id="9bcd4-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9bcd4-123">None</span></span>

## <span data-ttu-id="9bcd4-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bcd4-124">OUTPUTS</span></span>

### <span data-ttu-id="9bcd4-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="9bcd4-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="9bcd4-126">Notas</span><span class="sxs-lookup"><span data-stu-id="9bcd4-126">NOTES</span></span>

## <span data-ttu-id="9bcd4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bcd4-127">RELATED LINKS</span></span>
