---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113809"
---
# <span data-ttu-id="fb81e-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="fb81e-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="fb81e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb81e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb81e-103">Desabilita o monitoramento em um cluster HDInsight, e logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento especificado durante a habilitação.</span><span class="sxs-lookup"><span data-stu-id="fb81e-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="fb81e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb81e-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb81e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb81e-105">DESCRIPTION</span></span>
<span data-ttu-id="fb81e-106">O cmdlet **Disable-AzHDInsightMonitoring** desabilita o monitoramento em um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb81e-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fb81e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb81e-107">EXAMPLES</span></span>

### <span data-ttu-id="fb81e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb81e-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="fb81e-109">O monitoramento será desabilitado no cluster HDInsight e logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="fb81e-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="fb81e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb81e-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="fb81e-111">O monitoramento será desabilitado no cluster HDInsight e logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="fb81e-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="fb81e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb81e-112">PARAMETERS</span></span>

### <span data-ttu-id="fb81e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb81e-113">-DefaultProfile</span></span>
<span data-ttu-id="fb81e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fb81e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb81e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb81e-115">-Name</span></span>
<span data-ttu-id="fb81e-116">O nome do cluster para desabilitar o Monitoramento.</span><span class="sxs-lookup"><span data-stu-id="fb81e-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="fb81e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb81e-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb81e-118">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="fb81e-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="fb81e-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fb81e-119">-Confirm</span></span>
<span data-ttu-id="fb81e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb81e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb81e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb81e-121">-WhatIf</span></span>
<span data-ttu-id="fb81e-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fb81e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb81e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb81e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb81e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb81e-124">CommonParameters</span></span>
<span data-ttu-id="fb81e-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb81e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb81e-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb81e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb81e-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb81e-127">INPUTS</span></span>

### <span data-ttu-id="fb81e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fb81e-128">System.String</span></span>

## <span data-ttu-id="fb81e-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb81e-129">OUTPUTS</span></span>

### <span data-ttu-id="fb81e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb81e-130">System.Boolean</span></span>

## <span data-ttu-id="fb81e-131">Notas</span><span class="sxs-lookup"><span data-stu-id="fb81e-131">NOTES</span></span>

## <span data-ttu-id="fb81e-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb81e-132">RELATED LINKS</span></span>
