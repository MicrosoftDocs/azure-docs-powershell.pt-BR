---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429313"
---
# <span data-ttu-id="17cad-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="17cad-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="17cad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17cad-102">SYNOPSIS</span></span>
<span data-ttu-id="17cad-103">Habilita o monitoramento em um cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho monitoramento especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="17cad-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="17cad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17cad-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17cad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17cad-105">DESCRIPTION</span></span>
<span data-ttu-id="17cad-106">O cmdlet **Enable-AzHDInsightMonitoring** habilita o monitoramento em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="17cad-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="17cad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17cad-107">EXAMPLES</span></span>

### <span data-ttu-id="17cad-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17cad-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="17cad-109">O monitoramento será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho monitoramento com ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="17cad-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="17cad-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17cad-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="17cad-111">O monitoramento será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho monitoramento com ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="17cad-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="17cad-112">OS</span><span class="sxs-lookup"><span data-stu-id="17cad-112">PARAMETERS</span></span>

### <span data-ttu-id="17cad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17cad-113">-DefaultProfile</span></span>
<span data-ttu-id="17cad-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="17cad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17cad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="17cad-115">-Name</span></span>
<span data-ttu-id="17cad-116">O nome do cluster para habilitar o monitoramento.</span><span class="sxs-lookup"><span data-stu-id="17cad-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="17cad-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="17cad-117">-PrimaryKey</span></span>
<span data-ttu-id="17cad-118">A chave primária do espaço de trabalho monitoramento.</span><span class="sxs-lookup"><span data-stu-id="17cad-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="17cad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17cad-119">-ResourceGroupName</span></span>
<span data-ttu-id="17cad-120">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="17cad-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="17cad-121">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="17cad-121">-WorkspaceId</span></span>
<span data-ttu-id="17cad-122">A ID do espaço de trabalho de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="17cad-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="17cad-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17cad-123">-Confirm</span></span>
<span data-ttu-id="17cad-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17cad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17cad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17cad-125">-WhatIf</span></span>
<span data-ttu-id="17cad-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17cad-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17cad-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17cad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17cad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17cad-128">CommonParameters</span></span>
<span data-ttu-id="17cad-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17cad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17cad-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17cad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17cad-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17cad-131">INPUTS</span></span>

### <span data-ttu-id="17cad-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17cad-132">System.String</span></span>

## <span data-ttu-id="17cad-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17cad-133">OUTPUTS</span></span>

### <span data-ttu-id="17cad-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17cad-134">System.Boolean</span></span>

## <span data-ttu-id="17cad-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17cad-135">NOTES</span></span>

## <span data-ttu-id="17cad-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17cad-136">RELATED LINKS</span></span>
