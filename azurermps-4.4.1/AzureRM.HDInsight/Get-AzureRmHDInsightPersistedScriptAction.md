---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610790"
---
# <span data-ttu-id="a6b33-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a6b33-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a6b33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6b33-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b33-103">Obtém as ações de script persistente para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="a6b33-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6b33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6b33-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6b33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6b33-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b33-106">O cmdlet **Get-AzureRmHDInsightPersistedScriptAction** Obtém as ações de script persistentes para um cluster do Azure HDInsight e lista-as em ordem cronológica ou obtém os detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="a6b33-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a6b33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6b33-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b33-108">Exemplo 1: obter as ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="a6b33-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a6b33-109">Este comando obtém ações de script persistentes no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a6b33-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a6b33-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6b33-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b33-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a6b33-111">-ClusterName</span></span>
<span data-ttu-id="a6b33-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a6b33-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a6b33-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6b33-113">-Name</span></span>
<span data-ttu-id="a6b33-114">Especifica o nome da ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="a6b33-114">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="a6b33-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b33-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6b33-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6b33-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a6b33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b33-117">-DefaultProfile</span></span>
<span data-ttu-id="a6b33-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6b33-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b33-119">CommonParameters</span></span>
<span data-ttu-id="a6b33-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6b33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b33-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b33-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b33-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6b33-122">INPUTS</span></span>

## <span data-ttu-id="a6b33-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6b33-123">OUTPUTS</span></span>

### <span data-ttu-id="a6b33-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="a6b33-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="a6b33-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6b33-125">NOTES</span></span>

## <span data-ttu-id="a6b33-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6b33-126">RELATED LINKS</span></span>

[<span data-ttu-id="a6b33-127">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a6b33-127">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a6b33-128">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a6b33-128">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


