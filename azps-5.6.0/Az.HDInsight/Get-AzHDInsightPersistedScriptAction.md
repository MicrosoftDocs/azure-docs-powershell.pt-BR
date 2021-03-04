---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 136099b4fb37952825afbf82ba99a11695b901a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892790"
---
# <span data-ttu-id="f84b6-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f84b6-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="f84b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84b6-102">SYNOPSIS</span></span>
<span data-ttu-id="f84b6-103">Obtém as ações de script persistentes para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificada.</span><span class="sxs-lookup"><span data-stu-id="f84b6-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="f84b6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f84b6-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f84b6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f84b6-105">DESCRIPTION</span></span>
<span data-ttu-id="f84b6-106">O cmdlet **Get-AzHDInsightPersistedScriptAction** obtém as ações de script persistentes para um cluster HDInsight do Azure e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificada.</span><span class="sxs-lookup"><span data-stu-id="f84b6-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="f84b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f84b6-107">EXAMPLES</span></span>

### <span data-ttu-id="f84b6-108">Exemplo 1: Obter as ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="f84b6-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="f84b6-109">Esse comando obtém ações de script persistentes no cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f84b6-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f84b6-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f84b6-110">PARAMETERS</span></span>

### <span data-ttu-id="f84b6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f84b6-111">-ClusterName</span></span>
<span data-ttu-id="f84b6-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="f84b6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f84b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84b6-113">-DefaultProfile</span></span>
<span data-ttu-id="f84b6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f84b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f84b6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f84b6-115">-Name</span></span>
<span data-ttu-id="f84b6-116">Especifica o nome da ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="f84b6-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="f84b6-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f84b6-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f84b6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84b6-119">CommonParameters</span></span>
<span data-ttu-id="f84b6-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84b6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84b6-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f84b6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84b6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f84b6-122">INPUTS</span></span>

### <span data-ttu-id="f84b6-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f84b6-123">None</span></span>

## <span data-ttu-id="f84b6-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f84b6-124">OUTPUTS</span></span>

### <span data-ttu-id="f84b6-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="f84b6-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="f84b6-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="f84b6-126">NOTES</span></span>

## <span data-ttu-id="f84b6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f84b6-127">RELATED LINKS</span></span>

[<span data-ttu-id="f84b6-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f84b6-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="f84b6-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f84b6-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


