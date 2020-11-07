---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784897"
---
# <span data-ttu-id="98c98-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="98c98-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="98c98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98c98-102">SYNOPSIS</span></span>
<span data-ttu-id="98c98-103">Desabilita o monitoramento em um cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="98c98-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="98c98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98c98-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c98-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98c98-105">DESCRIPTION</span></span>
<span data-ttu-id="98c98-106">O cmdlet **Disable-AzHDInsightMonitoring** desabilita o monitoramento em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="98c98-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="98c98-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98c98-107">EXAMPLES</span></span>

### <span data-ttu-id="98c98-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98c98-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="98c98-109">O monitoramento será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho monitoramento.</span><span class="sxs-lookup"><span data-stu-id="98c98-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="98c98-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="98c98-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="98c98-111">O monitoramento será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho monitoramento.</span><span class="sxs-lookup"><span data-stu-id="98c98-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="98c98-112">OS</span><span class="sxs-lookup"><span data-stu-id="98c98-112">PARAMETERS</span></span>

### <span data-ttu-id="98c98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c98-113">-DefaultProfile</span></span>
<span data-ttu-id="98c98-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="98c98-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98c98-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="98c98-115">-Name</span></span>
<span data-ttu-id="98c98-116">O nome do cluster para desabilitar o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="98c98-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="98c98-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c98-117">-ResourceGroupName</span></span>
<span data-ttu-id="98c98-118">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="98c98-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="98c98-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98c98-119">-Confirm</span></span>
<span data-ttu-id="98c98-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c98-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c98-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c98-121">-WhatIf</span></span>
<span data-ttu-id="98c98-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98c98-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c98-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98c98-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c98-124">CommonParameters</span></span>
<span data-ttu-id="98c98-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c98-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c98-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c98-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98c98-127">INPUTS</span></span>

### <span data-ttu-id="98c98-128">System. String</span><span class="sxs-lookup"><span data-stu-id="98c98-128">System.String</span></span>

## <span data-ttu-id="98c98-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98c98-129">OUTPUTS</span></span>

### <span data-ttu-id="98c98-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98c98-130">System.Boolean</span></span>

## <span data-ttu-id="98c98-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98c98-131">NOTES</span></span>

## <span data-ttu-id="98c98-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98c98-132">RELATED LINKS</span></span>
