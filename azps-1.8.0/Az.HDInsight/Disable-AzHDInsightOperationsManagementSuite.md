---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 4f4508d38e4401198359fc816d1a94875f70940a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770811"
---
# <span data-ttu-id="af3fc-101">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="af3fc-101">Disable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="af3fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="af3fc-103">Desabilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="af3fc-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="af3fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af3fc-104">SYNTAX</span></span>

```
Disable-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af3fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="af3fc-106">O cmdlet **Disable-AzHDInsightOperationsManagementSuite** DESABILITA o OMS (Operations Management Suite) em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="af3fc-106">The **Disable-AzHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="af3fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af3fc-107">EXAMPLES</span></span>

### <span data-ttu-id="af3fc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af3fc-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="af3fc-109">O Operations Management Suite (OMS) será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="af3fc-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="af3fc-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af3fc-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="af3fc-111">O Operations Management Suite (OMS) será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="af3fc-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="af3fc-112">OS</span><span class="sxs-lookup"><span data-stu-id="af3fc-112">PARAMETERS</span></span>

### <span data-ttu-id="af3fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3fc-113">-DefaultProfile</span></span>
<span data-ttu-id="af3fc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af3fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af3fc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="af3fc-115">-Name</span></span>
<span data-ttu-id="af3fc-116">O nome do cluster para desabilitar o OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="af3fc-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="af3fc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3fc-117">-ResourceGroupName</span></span>
<span data-ttu-id="af3fc-118">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="af3fc-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="af3fc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af3fc-119">-Confirm</span></span>
<span data-ttu-id="af3fc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af3fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3fc-121">-WhatIf</span></span>
<span data-ttu-id="af3fc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af3fc-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af3fc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af3fc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3fc-124">CommonParameters</span></span>
<span data-ttu-id="af3fc-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af3fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3fc-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af3fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3fc-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af3fc-127">INPUTS</span></span>

### <span data-ttu-id="af3fc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af3fc-128">System.String</span></span>

## <span data-ttu-id="af3fc-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af3fc-129">OUTPUTS</span></span>

### <span data-ttu-id="af3fc-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="af3fc-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="af3fc-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af3fc-131">NOTES</span></span>

## <span data-ttu-id="af3fc-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af3fc-132">RELATED LINKS</span></span>
