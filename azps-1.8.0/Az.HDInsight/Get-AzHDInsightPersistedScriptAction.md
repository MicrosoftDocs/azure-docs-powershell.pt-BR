---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a437c27aaa5caea7ae0efb7ab477fe643a5c80a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770806"
---
# <span data-ttu-id="fa136-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fa136-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="fa136-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa136-102">SYNOPSIS</span></span>
<span data-ttu-id="fa136-103">Obtém as ações de script persistente para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="fa136-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="fa136-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa136-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa136-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa136-105">DESCRIPTION</span></span>
<span data-ttu-id="fa136-106">O cmdlet **Get-AzHDInsightPersistedScriptAction** Obtém as ações de script persistentes para um cluster do Azure HDInsight e lista-as em ordem cronológica ou obtém os detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="fa136-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="fa136-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa136-107">EXAMPLES</span></span>

### <span data-ttu-id="fa136-108">Exemplo 1: obter as ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="fa136-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="fa136-109">Este comando obtém ações de script persistentes no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="fa136-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fa136-110">OS</span><span class="sxs-lookup"><span data-stu-id="fa136-110">PARAMETERS</span></span>

### <span data-ttu-id="fa136-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fa136-111">-ClusterName</span></span>
<span data-ttu-id="fa136-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="fa136-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fa136-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa136-113">-DefaultProfile</span></span>
<span data-ttu-id="fa136-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fa136-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa136-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa136-115">-Name</span></span>
<span data-ttu-id="fa136-116">Especifica o nome da ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="fa136-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="fa136-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa136-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa136-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa136-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fa136-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa136-119">CommonParameters</span></span>
<span data-ttu-id="fa136-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa136-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa136-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa136-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa136-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa136-122">INPUTS</span></span>

### <span data-ttu-id="fa136-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fa136-123">None</span></span>

## <span data-ttu-id="fa136-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa136-124">OUTPUTS</span></span>

### <span data-ttu-id="fa136-125">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="fa136-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="fa136-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa136-126">NOTES</span></span>

## <span data-ttu-id="fa136-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa136-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa136-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fa136-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="fa136-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="fa136-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


