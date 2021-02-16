---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: f593989125642d03a9dff1b48bbc7430498b2a36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113186"
---
# <span data-ttu-id="228d9-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="228d9-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="228d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="228d9-102">SYNOPSIS</span></span>
<span data-ttu-id="228d9-103">Define uma ação de script executada anteriormente como uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="228d9-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="228d9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="228d9-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="228d9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="228d9-105">DESCRIPTION</span></span>
<span data-ttu-id="228d9-106">O cmdlet **Set-AzHDInsightPersistedScriptAction** define uma ação de script executada anteriormente para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="228d9-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="228d9-107">A ação de script especificada deve ter sido bem-sucedida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="228d9-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="228d9-108">A ação de script será executado sempre que o cluster HDInsight do Azure for dimensionado.</span><span class="sxs-lookup"><span data-stu-id="228d9-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="228d9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="228d9-109">EXAMPLES</span></span>

### <span data-ttu-id="228d9-110">Exemplo 1: Definir uma ação de script bem-sucedida anteriormente a ser persistente ou executar em escala de cluster</span><span class="sxs-lookup"><span data-stu-id="228d9-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="228d9-111">Esse comando define uma ação de script bem-sucedida anteriormente como uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="228d9-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="228d9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="228d9-112">PARAMETERS</span></span>

### <span data-ttu-id="228d9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="228d9-113">-ClusterName</span></span>
<span data-ttu-id="228d9-114">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="228d9-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="228d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228d9-115">-DefaultProfile</span></span>
<span data-ttu-id="228d9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="228d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="228d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="228d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="228d9-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="228d9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="228d9-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="228d9-119">-ScriptExecutionId</span></span>
<span data-ttu-id="228d9-120">Especifica a ID de execução da ação de script a ser promoveda como persistente.</span><span class="sxs-lookup"><span data-stu-id="228d9-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="228d9-121">Essa ação de script deve ter sido bem-sucedida para ser promovido.</span><span class="sxs-lookup"><span data-stu-id="228d9-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="228d9-122">Você pode encontrar a ID de execução de ação de script usando Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="228d9-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228d9-123">CommonParameters</span></span>
<span data-ttu-id="228d9-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228d9-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="228d9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228d9-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="228d9-126">INPUTS</span></span>

### <span data-ttu-id="228d9-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="228d9-127">None</span></span>

## <span data-ttu-id="228d9-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="228d9-128">OUTPUTS</span></span>

### <span data-ttu-id="228d9-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="228d9-129">System.Void</span></span>

## <span data-ttu-id="228d9-130">Notas</span><span class="sxs-lookup"><span data-stu-id="228d9-130">NOTES</span></span>

## <span data-ttu-id="228d9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="228d9-131">RELATED LINKS</span></span>

[<span data-ttu-id="228d9-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="228d9-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="228d9-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="228d9-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


