---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610659"
---
# <span data-ttu-id="b713b-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b713b-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b713b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b713b-102">SYNOPSIS</span></span>
<span data-ttu-id="b713b-103">Define uma ação de script executada anteriormente para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="b713b-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b713b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b713b-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b713b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b713b-105">DESCRIPTION</span></span>
<span data-ttu-id="b713b-106">O cmdlet **set-AzureRmHDInsightPersistedScriptAction** define uma ação de script executada anteriormente para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="b713b-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="b713b-107">A ação de script especificada deve ter sido bem-sucedida anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b713b-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="b713b-108">A ação de script será executada toda vez que o cluster do Azure HDInsight for ampliado.</span><span class="sxs-lookup"><span data-stu-id="b713b-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="b713b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b713b-109">EXAMPLES</span></span>

### <span data-ttu-id="b713b-110">Exemplo 1: definir uma ação de script previamente bem-sucedida para persistir ou executar em expansão do cluster</span><span class="sxs-lookup"><span data-stu-id="b713b-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="b713b-111">Esse comando define uma ação de script anterior bem-sucedida para ser uma ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="b713b-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="b713b-112">OS</span><span class="sxs-lookup"><span data-stu-id="b713b-112">PARAMETERS</span></span>

### <span data-ttu-id="b713b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b713b-113">-ClusterName</span></span>
<span data-ttu-id="b713b-114">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="b713b-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b713b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b713b-115">-DefaultProfile</span></span>
<span data-ttu-id="b713b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b713b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b713b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b713b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b713b-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b713b-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b713b-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="b713b-119">-ScriptExecutionId</span></span>
<span data-ttu-id="b713b-120">Especifica a ID de execução da ação de script a ser promovida para persistente.</span><span class="sxs-lookup"><span data-stu-id="b713b-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="b713b-121">Esta ação de script deve ter sido bem-sucedida para ser promovida.</span><span class="sxs-lookup"><span data-stu-id="b713b-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="b713b-122">Você pode encontrar a ID de execução da ação de script usando Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="b713b-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b713b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b713b-123">CommonParameters</span></span>
<span data-ttu-id="b713b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b713b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b713b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b713b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b713b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b713b-126">INPUTS</span></span>

### <span data-ttu-id="b713b-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b713b-127">None</span></span>
<span data-ttu-id="b713b-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b713b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b713b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b713b-129">OUTPUTS</span></span>

### <span data-ttu-id="b713b-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b713b-130">System.Void</span></span>

## <span data-ttu-id="b713b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b713b-131">NOTES</span></span>

## <span data-ttu-id="b713b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b713b-132">RELATED LINKS</span></span>

[<span data-ttu-id="b713b-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b713b-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b713b-134">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b713b-134">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


