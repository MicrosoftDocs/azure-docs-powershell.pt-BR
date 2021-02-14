---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116769"
---
# <span data-ttu-id="65b74-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="65b74-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="65b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65b74-102">SYNOPSIS</span></span>
<span data-ttu-id="65b74-103">Remove o cluster HDInsight especificado da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="65b74-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="65b74-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65b74-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b74-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="65b74-105">DESCRIPTION</span></span>
<span data-ttu-id="65b74-106">O cmdlet **Remove-AzHDInsightCluster** remove o cluster de serviço HDInsight especificado de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="65b74-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="65b74-107">Esta operação também exclui todos os dados armazenados no Sistema de Arquivos Distribuído Hadoop (HDFS) no cluster.</span><span class="sxs-lookup"><span data-stu-id="65b74-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="65b74-108">Os dados armazenados na conta de Armazenamento do Azure associada não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="65b74-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="65b74-109">Os dados armazenados em metadados externos não são excluídos.</span><span class="sxs-lookup"><span data-stu-id="65b74-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="65b74-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65b74-110">EXAMPLES</span></span>

### <span data-ttu-id="65b74-111">Exemplo 1: Excluir um cluster HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="65b74-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="65b74-112">Esse comando remove o cluster chamado hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="65b74-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="65b74-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65b74-113">PARAMETERS</span></span>

### <span data-ttu-id="65b74-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="65b74-114">-ClusterName</span></span>
<span data-ttu-id="65b74-115">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="65b74-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="65b74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b74-116">-DefaultProfile</span></span>
<span data-ttu-id="65b74-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="65b74-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65b74-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65b74-118">-PassThru</span></span>
<span data-ttu-id="65b74-119">Se PassThru estiver presente, saída do resultado</span><span class="sxs-lookup"><span data-stu-id="65b74-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b74-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b74-120">-ResourceGroupName</span></span>
<span data-ttu-id="65b74-121">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65b74-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="65b74-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b74-122">CommonParameters</span></span>
<span data-ttu-id="65b74-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b74-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b74-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65b74-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b74-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="65b74-125">INPUTS</span></span>

### <span data-ttu-id="65b74-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65b74-126">None</span></span>
## <span data-ttu-id="65b74-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="65b74-127">OUTPUTS</span></span>

### <span data-ttu-id="65b74-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65b74-128">System.Boolean</span></span>
## <span data-ttu-id="65b74-129">Notas</span><span class="sxs-lookup"><span data-stu-id="65b74-129">NOTES</span></span>

## <span data-ttu-id="65b74-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65b74-130">RELATED LINKS</span></span>

[<span data-ttu-id="65b74-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="65b74-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="65b74-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="65b74-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


