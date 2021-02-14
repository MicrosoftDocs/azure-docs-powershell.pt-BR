---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116767"
---
# <span data-ttu-id="3f8b7-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3f8b7-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="3f8b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8b7-103">Remove uma ação de script persistente de um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="3f8b7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f8b7-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f8b7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="3f8b7-106">O cmdlet **Remove-AzHDInsightPersistedScriptAction** remove uma ação de script persistente da lista de ações de script persistente do cluster Azure HDInsight especificada.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="3f8b7-107">O script removido não será mais executado quando o cluster for dimensionado.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="3f8b7-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f8b7-108">EXAMPLES</span></span>

### <span data-ttu-id="3f8b7-109">Exemplo 1: Remover uma ação de script da lista de ações de script persistente em um cluster</span><span class="sxs-lookup"><span data-stu-id="3f8b7-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="3f8b7-110">Esse comando remove a ação de script chamada Scriptaction da lista de ações de script persistentes no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="3f8b7-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f8b7-111">PARAMETERS</span></span>

### <span data-ttu-id="3f8b7-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f8b7-112">-ClusterName</span></span>
<span data-ttu-id="3f8b7-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3f8b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8b7-114">-DefaultProfile</span></span>
<span data-ttu-id="3f8b7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3f8b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f8b7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f8b7-116">-Name</span></span>
<span data-ttu-id="3f8b7-117">Especifica o nome da ação de script persistente a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="3f8b7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8b7-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f8b7-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3f8b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8b7-120">CommonParameters</span></span>
<span data-ttu-id="3f8b7-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f8b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8b7-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f8b7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8b7-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f8b7-123">INPUTS</span></span>

### <span data-ttu-id="3f8b7-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3f8b7-124">None</span></span>

## <span data-ttu-id="3f8b7-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f8b7-125">OUTPUTS</span></span>

### <span data-ttu-id="3f8b7-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f8b7-126">System.Void</span></span>

## <span data-ttu-id="3f8b7-127">Notas</span><span class="sxs-lookup"><span data-stu-id="3f8b7-127">NOTES</span></span>

## <span data-ttu-id="3f8b7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f8b7-128">RELATED LINKS</span></span>

[<span data-ttu-id="3f8b7-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3f8b7-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="3f8b7-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3f8b7-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


