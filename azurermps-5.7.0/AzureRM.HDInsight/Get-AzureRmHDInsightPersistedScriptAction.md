---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441341"
---
# <span data-ttu-id="79030-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79030-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="79030-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79030-102">SYNOPSIS</span></span>
<span data-ttu-id="79030-103">Obtém as ações de script persistente para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="79030-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79030-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79030-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79030-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79030-105">DESCRIPTION</span></span>
<span data-ttu-id="79030-106">O cmdlet **Get-AzureRmHDInsightPersistedScriptAction** Obtém as ações de script persistentes para um cluster do Azure HDInsight e lista-as em ordem cronológica ou obtém os detalhes de uma ação de script persistente especificado.</span><span class="sxs-lookup"><span data-stu-id="79030-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="79030-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79030-107">EXAMPLES</span></span>

### <span data-ttu-id="79030-108">Exemplo 1: obter as ações de script persistentes em um cluster</span><span class="sxs-lookup"><span data-stu-id="79030-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="79030-109">Este comando obtém ações de script persistentes no cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="79030-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="79030-110">OS</span><span class="sxs-lookup"><span data-stu-id="79030-110">PARAMETERS</span></span>

### <span data-ttu-id="79030-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79030-111">-ClusterName</span></span>
<span data-ttu-id="79030-112">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="79030-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="79030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79030-113">-DefaultProfile</span></span>
<span data-ttu-id="79030-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="79030-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79030-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="79030-115">-Name</span></span>
<span data-ttu-id="79030-116">Especifica o nome da ação de script persistente.</span><span class="sxs-lookup"><span data-stu-id="79030-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79030-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79030-117">-ResourceGroupName</span></span>
<span data-ttu-id="79030-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="79030-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="79030-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79030-119">CommonParameters</span></span>
<span data-ttu-id="79030-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79030-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79030-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79030-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79030-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79030-122">INPUTS</span></span>

### <span data-ttu-id="79030-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79030-123">None</span></span>
<span data-ttu-id="79030-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="79030-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79030-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79030-125">OUTPUTS</span></span>

### <span data-ttu-id="79030-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="79030-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="79030-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79030-127">NOTES</span></span>

## <span data-ttu-id="79030-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79030-128">RELATED LINKS</span></span>

[<span data-ttu-id="79030-129">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79030-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="79030-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="79030-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


