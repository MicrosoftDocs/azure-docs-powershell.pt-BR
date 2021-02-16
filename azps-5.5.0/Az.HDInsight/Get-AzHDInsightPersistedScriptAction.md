---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118470"
---
# <span data-ttu-id="015b9-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="015b9-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="015b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="015b9-102">SYNOPSIS</span></span>
<span data-ttu-id="015b9-103">Obtém as ações de script persistentes de um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificada.</span><span class="sxs-lookup"><span data-stu-id="015b9-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="015b9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="015b9-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="015b9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="015b9-105">DESCRIPTION</span></span>
<span data-ttu-id="015b9-106">O cmdlet **Get-AzHDInsightPersistedScriptAction** obtém as ações de script persistentes de um cluster HDInsight do Azure e as lista em ordem cronológica ou obtém detalhes de uma ação de script especificada.</span><span class="sxs-lookup"><span data-stu-id="015b9-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="015b9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="015b9-107">EXAMPLES</span></span>

### <span data-ttu-id="015b9-108">Exemplo 1: Obter as ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="015b9-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="015b9-109">Esse comando recebe ações de script persistentes no cluster chamado seu-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="015b9-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="015b9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="015b9-110">PARAMETERS</span></span>

### <span data-ttu-id="015b9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="015b9-111">-ClusterName</span></span>
<span data-ttu-id="015b9-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="015b9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="015b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015b9-113">-DefaultProfile</span></span>
<span data-ttu-id="015b9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="015b9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="015b9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="015b9-115">-Name</span></span>
<span data-ttu-id="015b9-116">Especifica o nome da ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="015b9-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="015b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="015b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="015b9-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="015b9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="015b9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015b9-119">CommonParameters</span></span>
<span data-ttu-id="015b9-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015b9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015b9-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="015b9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015b9-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="015b9-122">INPUTS</span></span>

### <span data-ttu-id="015b9-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="015b9-123">None</span></span>

## <span data-ttu-id="015b9-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="015b9-124">OUTPUTS</span></span>

### <span data-ttu-id="015b9-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="015b9-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="015b9-126">Notas</span><span class="sxs-lookup"><span data-stu-id="015b9-126">NOTES</span></span>

## <span data-ttu-id="015b9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="015b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="015b9-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="015b9-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="015b9-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="015b9-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


