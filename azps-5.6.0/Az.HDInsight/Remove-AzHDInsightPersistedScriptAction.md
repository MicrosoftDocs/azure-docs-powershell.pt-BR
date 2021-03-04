---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a7c5c9c2008839d4e90dd5f393fbe4acea0f78a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887122"
---
# <span data-ttu-id="9cb47-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9cb47-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="9cb47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb47-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb47-103">Remove uma ação de script persistente de um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9cb47-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="9cb47-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9cb47-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cb47-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9cb47-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb47-106">O cmdlet **Remove-AzHDInsightPersistedScriptAction** remove uma ação de script persistente da lista de ações de script persistentes do cluster HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="9cb47-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="9cb47-107">O script removido não será mais executado quando o cluster for ampliado.</span><span class="sxs-lookup"><span data-stu-id="9cb47-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="9cb47-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cb47-108">EXAMPLES</span></span>

### <span data-ttu-id="9cb47-109">Exemplo 1: Remover uma ação de script da lista de ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="9cb47-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="9cb47-110">Este comando remove a ação de script chamada Scriptaction da lista de ações de script persistentes no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="9cb47-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="9cb47-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9cb47-111">PARAMETERS</span></span>

### <span data-ttu-id="9cb47-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9cb47-112">-ClusterName</span></span>
<span data-ttu-id="9cb47-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="9cb47-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9cb47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb47-114">-DefaultProfile</span></span>
<span data-ttu-id="9cb47-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9cb47-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cb47-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9cb47-116">-Name</span></span>
<span data-ttu-id="9cb47-117">Especifica o nome da ação de script persistente a ser removida.</span><span class="sxs-lookup"><span data-stu-id="9cb47-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb47-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb47-118">-ResourceGroupName</span></span>
<span data-ttu-id="9cb47-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9cb47-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9cb47-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb47-120">CommonParameters</span></span>
<span data-ttu-id="9cb47-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb47-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb47-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb47-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb47-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cb47-123">INPUTS</span></span>

### <span data-ttu-id="9cb47-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9cb47-124">None</span></span>

## <span data-ttu-id="9cb47-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9cb47-125">OUTPUTS</span></span>

### <span data-ttu-id="9cb47-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="9cb47-126">System.Void</span></span>

## <span data-ttu-id="9cb47-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="9cb47-127">NOTES</span></span>

## <span data-ttu-id="9cb47-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cb47-128">RELATED LINKS</span></span>

[<span data-ttu-id="9cb47-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9cb47-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="9cb47-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="9cb47-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


