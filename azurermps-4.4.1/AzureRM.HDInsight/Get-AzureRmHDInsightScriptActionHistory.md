---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: 5e3ee9de0adf511407013ef346a2867cb43fb11c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441076"
---
# <span data-ttu-id="976c1-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="976c1-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="976c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="976c1-102">SYNOPSIS</span></span>
<span data-ttu-id="976c1-103">Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="976c1-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="976c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="976c1-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="976c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="976c1-105">DESCRIPTION</span></span>
<span data-ttu-id="976c1-106">O cmdlet **Get-AzureRmHDInsightScriptActionHistory** Obtém o histórico da ação de script de um cluster do Azure HDInsight e o lista em ordem cronológica inversa, ou obtém detalhes de uma ação de script executada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="976c1-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="976c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="976c1-107">EXAMPLES</span></span>

### <span data-ttu-id="976c1-108">Exemplo 1: obter o histórico de execuções de ações de script para um cluster</span><span class="sxs-lookup"><span data-stu-id="976c1-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="976c1-109">Esse comando obtém o histórico de ações de script para o cluster seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="976c1-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="976c1-110">OS</span><span class="sxs-lookup"><span data-stu-id="976c1-110">PARAMETERS</span></span>

### <span data-ttu-id="976c1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="976c1-111">-ClusterName</span></span>
<span data-ttu-id="976c1-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="976c1-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="976c1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976c1-113">-ResourceGroupName</span></span>
<span data-ttu-id="976c1-114">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="976c1-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="976c1-115">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="976c1-115">-ScriptExecutionId</span></span>
<span data-ttu-id="976c1-116">Especifica a ID de execução da ação de script executada.</span><span class="sxs-lookup"><span data-stu-id="976c1-116">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="976c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976c1-117">-DefaultProfile</span></span>
<span data-ttu-id="976c1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="976c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="976c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976c1-119">CommonParameters</span></span>
<span data-ttu-id="976c1-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976c1-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976c1-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="976c1-122">INPUTS</span></span>

## <span data-ttu-id="976c1-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="976c1-123">OUTPUTS</span></span>

### <span data-ttu-id="976c1-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="976c1-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="976c1-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="976c1-125">NOTES</span></span>

## <span data-ttu-id="976c1-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="976c1-126">RELATED LINKS</span></span>

