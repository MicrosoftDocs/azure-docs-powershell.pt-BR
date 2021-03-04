---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889466"
---
# <span data-ttu-id="4fd25-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4fd25-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="4fd25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fd25-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd25-103">Define uma ação de script executada anteriormente como uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="4fd25-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="4fd25-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4fd25-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd25-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4fd25-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd25-106">O cmdlet **Set-AzHDInsightPersistedScriptAction** define uma ação de script executada anteriormente como uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="4fd25-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="4fd25-107">A ação de script especificada deve ter sido bem-sucedida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4fd25-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="4fd25-108">A ação de script será executado sempre que o cluster HDInsight do Azure for ampliado.</span><span class="sxs-lookup"><span data-stu-id="4fd25-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="4fd25-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fd25-109">EXAMPLES</span></span>

### <span data-ttu-id="4fd25-110">Exemplo 1: definir uma ação de script bem-sucedida anteriormente a ser persistente ou executar em escala de cluster</span><span class="sxs-lookup"><span data-stu-id="4fd25-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="4fd25-111">Este comando define uma ação de script bem-sucedida anteriormente como uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="4fd25-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="4fd25-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4fd25-112">PARAMETERS</span></span>

### <span data-ttu-id="4fd25-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4fd25-113">-ClusterName</span></span>
<span data-ttu-id="4fd25-114">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4fd25-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4fd25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd25-115">-DefaultProfile</span></span>
<span data-ttu-id="4fd25-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4fd25-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fd25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd25-117">-ResourceGroupName</span></span>
<span data-ttu-id="4fd25-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fd25-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4fd25-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="4fd25-119">-ScriptExecutionId</span></span>
<span data-ttu-id="4fd25-120">Especifica a ID de execução da ação de script para promover a persistência.</span><span class="sxs-lookup"><span data-stu-id="4fd25-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="4fd25-121">Essa ação de script deve ter sido bem-sucedida para ser promovido.</span><span class="sxs-lookup"><span data-stu-id="4fd25-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="4fd25-122">Você pode encontrar a ID de execução de ação de script usando Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="4fd25-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="4fd25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd25-123">CommonParameters</span></span>
<span data-ttu-id="4fd25-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd25-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fd25-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd25-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fd25-126">INPUTS</span></span>

### <span data-ttu-id="4fd25-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4fd25-127">None</span></span>

## <span data-ttu-id="4fd25-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4fd25-128">OUTPUTS</span></span>

### <span data-ttu-id="4fd25-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="4fd25-129">System.Void</span></span>

## <span data-ttu-id="4fd25-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="4fd25-130">NOTES</span></span>

## <span data-ttu-id="4fd25-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fd25-131">RELATED LINKS</span></span>

[<span data-ttu-id="4fd25-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4fd25-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="4fd25-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="4fd25-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


