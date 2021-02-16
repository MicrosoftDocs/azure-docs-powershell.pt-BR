---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117635"
---
# <span data-ttu-id="30115-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="30115-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="30115-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30115-102">SYNOPSIS</span></span>
<span data-ttu-id="30115-103">Reinicia os hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30115-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="30115-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30115-104">SYNTAX</span></span>

### <span data-ttu-id="30115-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30115-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30115-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="30115-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30115-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="30115-107">DESCRIPTION</span></span>
<span data-ttu-id="30115-108">Este cmdlet **Restart-AzHDInsightHost** reinicia os hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30115-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="30115-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30115-109">EXAMPLES</span></span>

### <span data-ttu-id="30115-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30115-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="30115-111">Este comando reinicia dois hosts do cluster: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="30115-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="30115-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="30115-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="30115-113">Este comando mostra como colaborar com o cmdlet 'Get-AzHDInsightHost'.</span><span class="sxs-lookup"><span data-stu-id="30115-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="30115-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30115-114">PARAMETERS</span></span>

### <span data-ttu-id="30115-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30115-115">-AsJob</span></span>
<span data-ttu-id="30115-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="30115-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30115-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="30115-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="30115-118">Obtém ou define o nome do host.</span><span class="sxs-lookup"><span data-stu-id="30115-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30115-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30115-119">-ClusterName</span></span>
<span data-ttu-id="30115-120">Obtém ou define o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="30115-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="30115-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30115-121">-DefaultProfile</span></span>
<span data-ttu-id="30115-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30115-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30115-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="30115-123">-Name</span></span>
<span data-ttu-id="30115-124">Obtém ou define o nome do host.</span><span class="sxs-lookup"><span data-stu-id="30115-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30115-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30115-125">-PassThru</span></span>
<span data-ttu-id="30115-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="30115-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="30115-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30115-127">-ResourceGroupName</span></span>
<span data-ttu-id="30115-128">Obtém ou define o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30115-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30115-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="30115-129">-Confirm</span></span>
<span data-ttu-id="30115-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30115-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30115-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30115-131">-WhatIf</span></span>
<span data-ttu-id="30115-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="30115-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30115-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30115-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30115-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30115-134">CommonParameters</span></span>
<span data-ttu-id="30115-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30115-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30115-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30115-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30115-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="30115-137">INPUTS</span></span>

### <span data-ttu-id="30115-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="30115-138">System.String[]</span></span>

### <span data-ttu-id="30115-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="30115-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="30115-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="30115-140">OUTPUTS</span></span>

### <span data-ttu-id="30115-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30115-141">System.Boolean</span></span>

## <span data-ttu-id="30115-142">Notas</span><span class="sxs-lookup"><span data-stu-id="30115-142">NOTES</span></span>

## <span data-ttu-id="30115-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30115-143">RELATED LINKS</span></span>
