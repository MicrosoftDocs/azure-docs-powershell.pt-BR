---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955560"
---
# <span data-ttu-id="5711f-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5711f-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5711f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5711f-102">SYNOPSIS</span></span>
<span data-ttu-id="5711f-103">Define uma ação de script executada anteriormente para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="5711f-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="5711f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5711f-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5711f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5711f-105">DESCRIPTION</span></span>
<span data-ttu-id="5711f-106">O cmdlet **set-AzHDInsightPersistedScriptAction** define uma ação de script executada anteriormente para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="5711f-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="5711f-107">A ação de script especificada deve ter sido bem-sucedida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5711f-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="5711f-108">A ação de script será executada toda vez que o cluster do Azure HDInsight for ampliado.</span><span class="sxs-lookup"><span data-stu-id="5711f-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="5711f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5711f-109">EXAMPLES</span></span>

### <span data-ttu-id="5711f-110">Exemplo 1: definir uma ação de script previamente bem-sucedida para persistir ou executar em expansão do cluster</span><span class="sxs-lookup"><span data-stu-id="5711f-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="5711f-111">Esse comando define uma ação de script anterior bem-sucedida para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="5711f-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="5711f-112">OS</span><span class="sxs-lookup"><span data-stu-id="5711f-112">PARAMETERS</span></span>

### <span data-ttu-id="5711f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5711f-113">-ClusterName</span></span>
<span data-ttu-id="5711f-114">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="5711f-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5711f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5711f-115">-DefaultProfile</span></span>
<span data-ttu-id="5711f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5711f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5711f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5711f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5711f-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5711f-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5711f-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="5711f-119">-ScriptExecutionId</span></span>
<span data-ttu-id="5711f-120">Especifica a ID de execução da ação de script a ser promovida para persistente.</span><span class="sxs-lookup"><span data-stu-id="5711f-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="5711f-121">Esta ação de script deve ter sido bem-sucedida para ser promovida.</span><span class="sxs-lookup"><span data-stu-id="5711f-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="5711f-122">Você pode encontrar a ID de execução da ação de script usando Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="5711f-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="5711f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5711f-123">CommonParameters</span></span>
<span data-ttu-id="5711f-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5711f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5711f-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5711f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5711f-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5711f-126">INPUTS</span></span>

### <span data-ttu-id="5711f-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5711f-127">None</span></span>

## <span data-ttu-id="5711f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5711f-128">OUTPUTS</span></span>

### <span data-ttu-id="5711f-129">System. void</span><span class="sxs-lookup"><span data-stu-id="5711f-129">System.Void</span></span>

## <span data-ttu-id="5711f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5711f-130">NOTES</span></span>

## <span data-ttu-id="5711f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5711f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5711f-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5711f-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5711f-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5711f-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


