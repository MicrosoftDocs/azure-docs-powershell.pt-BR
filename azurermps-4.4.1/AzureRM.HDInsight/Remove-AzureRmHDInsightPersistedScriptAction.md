---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28526dd4aaa36890800a2bffd47eeae3f281d747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427932"
---
# <span data-ttu-id="474b9-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="474b9-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="474b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="474b9-102">SYNOPSIS</span></span>
<span data-ttu-id="474b9-103">Remove uma ação de script persistente de um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="474b9-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="474b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="474b9-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="474b9-105">DESCRIPTION</span></span>
<span data-ttu-id="474b9-106">O cmdlet **Remove-AzureRmHDInsightPersistedScriptAction** remove uma ação de script persistente da lista de ações de script persistentes do cluster do Azure HDInsight especificado.</span><span class="sxs-lookup"><span data-stu-id="474b9-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="474b9-107">O script removido não será mais executado quando o cluster estiver ampliado.</span><span class="sxs-lookup"><span data-stu-id="474b9-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="474b9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="474b9-108">EXAMPLES</span></span>

### <span data-ttu-id="474b9-109">Exemplo 1: remover uma ação de script da lista de ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="474b9-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="474b9-110">Esse comando Remove a ação de script chamada ScriptAction da lista de ações persistentes de script no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="474b9-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="474b9-111">OS</span><span class="sxs-lookup"><span data-stu-id="474b9-111">PARAMETERS</span></span>

### <span data-ttu-id="474b9-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="474b9-112">-ClusterName</span></span>
<span data-ttu-id="474b9-113">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="474b9-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="474b9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="474b9-114">-Name</span></span>
<span data-ttu-id="474b9-115">Especifica o nome da ação de script persistente a ser removida.</span><span class="sxs-lookup"><span data-stu-id="474b9-115">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="474b9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474b9-116">-ResourceGroupName</span></span>
<span data-ttu-id="474b9-117">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="474b9-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="474b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474b9-118">-DefaultProfile</span></span>
<span data-ttu-id="474b9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="474b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="474b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474b9-120">CommonParameters</span></span>
<span data-ttu-id="474b9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474b9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474b9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474b9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="474b9-123">INPUTS</span></span>

## <span data-ttu-id="474b9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="474b9-124">OUTPUTS</span></span>

### <span data-ttu-id="474b9-125">System. void</span><span class="sxs-lookup"><span data-stu-id="474b9-125">System.Void</span></span>

## <span data-ttu-id="474b9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="474b9-126">NOTES</span></span>

## <span data-ttu-id="474b9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="474b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="474b9-128">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="474b9-128">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="474b9-129">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="474b9-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)

