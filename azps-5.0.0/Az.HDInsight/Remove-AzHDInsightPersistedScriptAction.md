---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280328"
---
# <span data-ttu-id="2d908-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2d908-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="2d908-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d908-102">SYNOPSIS</span></span>
<span data-ttu-id="2d908-103">Remove uma ação de script persistente de um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d908-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="2d908-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d908-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d908-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d908-105">DESCRIPTION</span></span>
<span data-ttu-id="2d908-106">O cmdlet **Remove-AzHDInsightPersistedScriptAction** remove uma ação de script persistente da lista de ações de script persistentes do cluster do Azure HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="2d908-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="2d908-107">O script removido não será mais executado quando o cluster estiver ampliado.</span><span class="sxs-lookup"><span data-stu-id="2d908-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="2d908-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d908-108">EXAMPLES</span></span>

### <span data-ttu-id="2d908-109">Exemplo 1: remover uma ação de script da lista de ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="2d908-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="2d908-110">Esse comando Remove a ação de script chamada ScriptAction da lista de ações persistentes de script no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="2d908-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="2d908-111">OS</span><span class="sxs-lookup"><span data-stu-id="2d908-111">PARAMETERS</span></span>

### <span data-ttu-id="2d908-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d908-112">-ClusterName</span></span>
<span data-ttu-id="2d908-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2d908-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2d908-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d908-114">-DefaultProfile</span></span>
<span data-ttu-id="2d908-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2d908-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d908-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d908-116">-Name</span></span>
<span data-ttu-id="2d908-117">Especifica o nome da ação de script persistente a ser removida.</span><span class="sxs-lookup"><span data-stu-id="2d908-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="2d908-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d908-118">-ResourceGroupName</span></span>
<span data-ttu-id="2d908-119">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d908-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d908-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d908-120">CommonParameters</span></span>
<span data-ttu-id="2d908-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d908-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d908-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d908-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d908-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d908-123">INPUTS</span></span>

### <span data-ttu-id="2d908-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2d908-124">None</span></span>

## <span data-ttu-id="2d908-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d908-125">OUTPUTS</span></span>

### <span data-ttu-id="2d908-126">System. void</span><span class="sxs-lookup"><span data-stu-id="2d908-126">System.Void</span></span>

## <span data-ttu-id="2d908-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d908-127">NOTES</span></span>

## <span data-ttu-id="2d908-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d908-128">RELATED LINKS</span></span>

[<span data-ttu-id="2d908-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2d908-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="2d908-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2d908-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


