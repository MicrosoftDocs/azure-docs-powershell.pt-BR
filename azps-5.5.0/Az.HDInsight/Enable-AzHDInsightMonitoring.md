---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111866"
---
# <span data-ttu-id="e354e-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="e354e-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="e354e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e354e-102">SYNOPSIS</span></span>
<span data-ttu-id="e354e-103">Habilita o monitoramento em um cluster HDInsight, e logs relevantes serão enviados para o espaço de trabalho de monitoramento especificado durante a habilitação.</span><span class="sxs-lookup"><span data-stu-id="e354e-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="e354e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e354e-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e354e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e354e-105">DESCRIPTION</span></span>
<span data-ttu-id="e354e-106">O cmdlet **Enable-AzHDInsightMonitoring** habilita o monitoramento em um cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="e354e-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e354e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e354e-107">EXAMPLES</span></span>

### <span data-ttu-id="e354e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e354e-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e354e-109">O monitoramento será habilitado no cluster HDInsight e logs relevantes serão enviados para o espaço de trabalho de monitoramento com id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="e354e-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="e354e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e354e-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="e354e-111">O monitoramento será habilitado no cluster HDInsight e logs relevantes serão enviados para o espaço de trabalho de monitoramento com id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="e354e-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="e354e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e354e-112">PARAMETERS</span></span>

### <span data-ttu-id="e354e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e354e-113">-DefaultProfile</span></span>
<span data-ttu-id="e354e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e354e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e354e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e354e-115">-Name</span></span>
<span data-ttu-id="e354e-116">O nome do cluster para habilitar o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="e354e-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="e354e-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e354e-117">-PrimaryKey</span></span>
<span data-ttu-id="e354e-118">A chave primária do espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="e354e-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e354e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e354e-119">-ResourceGroupName</span></span>
<span data-ttu-id="e354e-120">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="e354e-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="e354e-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e354e-121">-WorkspaceId</span></span>
<span data-ttu-id="e354e-122">A ID do espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="e354e-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="e354e-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e354e-123">-Confirm</span></span>
<span data-ttu-id="e354e-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e354e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e354e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e354e-125">-WhatIf</span></span>
<span data-ttu-id="e354e-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e354e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e354e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e354e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e354e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e354e-128">CommonParameters</span></span>
<span data-ttu-id="e354e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e354e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e354e-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e354e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e354e-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="e354e-131">INPUTS</span></span>

### <span data-ttu-id="e354e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e354e-132">System.String</span></span>

## <span data-ttu-id="e354e-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="e354e-133">OUTPUTS</span></span>

### <span data-ttu-id="e354e-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e354e-134">System.Boolean</span></span>

## <span data-ttu-id="e354e-135">Notas</span><span class="sxs-lookup"><span data-stu-id="e354e-135">NOTES</span></span>

## <span data-ttu-id="e354e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e354e-136">RELATED LINKS</span></span>
