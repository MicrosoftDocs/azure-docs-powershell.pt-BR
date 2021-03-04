---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887510"
---
# <span data-ttu-id="52979-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="52979-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="52979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52979-102">SYNOPSIS</span></span>
<span data-ttu-id="52979-103">Desabilita o monitoramento em um cluster HDInsight e os logs relevantes param de fluir para o espaço de trabalho de monitoramento especificado durante a habilitação.</span><span class="sxs-lookup"><span data-stu-id="52979-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="52979-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52979-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52979-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52979-105">DESCRIPTION</span></span>
<span data-ttu-id="52979-106">O cmdlet **Disable-AzHDInsightMonitoring** desabilita o monitoramento em um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="52979-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="52979-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52979-107">EXAMPLES</span></span>

### <span data-ttu-id="52979-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52979-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="52979-109">O monitoramento será desabilitado no cluster HDInsight e os logs relevantes param de fluir para o espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="52979-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="52979-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52979-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="52979-111">O monitoramento será desabilitado no cluster HDInsight e os logs relevantes param de fluir para o espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="52979-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="52979-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52979-112">PARAMETERS</span></span>

### <span data-ttu-id="52979-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52979-113">-DefaultProfile</span></span>
<span data-ttu-id="52979-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="52979-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52979-115">-Name</span><span class="sxs-lookup"><span data-stu-id="52979-115">-Name</span></span>
<span data-ttu-id="52979-116">O nome do cluster para desabilitar o Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="52979-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52979-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52979-117">-ResourceGroupName</span></span>
<span data-ttu-id="52979-118">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="52979-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52979-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52979-119">-Confirm</span></span>
<span data-ttu-id="52979-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52979-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52979-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52979-121">-WhatIf</span></span>
<span data-ttu-id="52979-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52979-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52979-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52979-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52979-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52979-124">CommonParameters</span></span>
<span data-ttu-id="52979-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52979-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52979-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52979-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52979-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52979-127">INPUTS</span></span>

### <span data-ttu-id="52979-128">System.String</span><span class="sxs-lookup"><span data-stu-id="52979-128">System.String</span></span>

## <span data-ttu-id="52979-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52979-129">OUTPUTS</span></span>

### <span data-ttu-id="52979-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52979-130">System.Boolean</span></span>

## <span data-ttu-id="52979-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="52979-131">NOTES</span></span>

## <span data-ttu-id="52979-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52979-132">RELATED LINKS</span></span>
