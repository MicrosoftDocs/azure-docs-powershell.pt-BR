---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770813"
---
# <span data-ttu-id="f4c0a-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="f4c0a-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="f4c0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c0a-103">Habilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="f4c0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4c0a-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4c0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c0a-106">O cmdlet **Enable-AzHDInsightOperationsManagementSuite** HABILITA o OMS (Operations Management Suite) em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f4c0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4c0a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4c0a-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="f4c0a-109">O serviço de gerenciamento de operações (OMS) será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS com a ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="f4c0a-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="f4c0a-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f4c0a-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="f4c0a-111">O serviço de gerenciamento de operações (OMS) será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS com a ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="f4c0a-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="f4c0a-112">OS</span><span class="sxs-lookup"><span data-stu-id="f4c0a-112">PARAMETERS</span></span>

### <span data-ttu-id="f4c0a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c0a-113">-DefaultProfile</span></span>
<span data-ttu-id="f4c0a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f4c0a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4c0a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4c0a-115">-Name</span></span>
<span data-ttu-id="f4c0a-116">O nome do cluster para habilitar o OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="f4c0a-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c0a-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f4c0a-117">-PrimaryKey</span></span>
<span data-ttu-id="f4c0a-118">A chave primária do espaço de trabalho do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="f4c0a-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="f4c0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4c0a-120">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="f4c0a-121">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="f4c0a-121">-WorkspaceId</span></span>
<span data-ttu-id="f4c0a-122">A ID do espaço de trabalho do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="f4c0a-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="f4c0a-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4c0a-123">-Confirm</span></span>
<span data-ttu-id="f4c0a-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c0a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c0a-125">-WhatIf</span></span>
<span data-ttu-id="f4c0a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c0a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c0a-128">CommonParameters</span></span>
<span data-ttu-id="f4c0a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c0a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c0a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4c0a-131">INPUTS</span></span>

### <span data-ttu-id="f4c0a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4c0a-132">System.String</span></span>

## <span data-ttu-id="f4c0a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4c0a-133">OUTPUTS</span></span>

### <span data-ttu-id="f4c0a-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="f4c0a-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="f4c0a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4c0a-135">NOTES</span></span>

## <span data-ttu-id="f4c0a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4c0a-136">RELATED LINKS</span></span>
