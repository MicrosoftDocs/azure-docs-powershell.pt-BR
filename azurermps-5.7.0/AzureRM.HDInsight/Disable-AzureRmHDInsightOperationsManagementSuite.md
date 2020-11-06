---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431681"
---
# <span data-ttu-id="efbb5-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="efbb5-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="efbb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="efbb5-103">Desabilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="efbb5-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efbb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efbb5-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efbb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="efbb5-105">DESCRIPTION</span></span>
<span data-ttu-id="efbb5-106">O cmdlet **Disable-AzureRmHDInsightOperationsManagementSuite** DESABILITA o OMS (Operations Management Suite) em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="efbb5-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="efbb5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="efbb5-107">EXAMPLES</span></span>

### <span data-ttu-id="efbb5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="efbb5-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="efbb5-109">O Operations Management Suite (OMS) será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="efbb5-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="efbb5-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="efbb5-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="efbb5-111">O Operations Management Suite (OMS) será desabilitado no cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS.</span><span class="sxs-lookup"><span data-stu-id="efbb5-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="efbb5-112">OS</span><span class="sxs-lookup"><span data-stu-id="efbb5-112">PARAMETERS</span></span>

### <span data-ttu-id="efbb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbb5-113">-DefaultProfile</span></span>
<span data-ttu-id="efbb5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="efbb5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efbb5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="efbb5-115">-Name</span></span>
<span data-ttu-id="efbb5-116">O nome do cluster para desabilitar o OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="efbb5-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efbb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efbb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="efbb5-118">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="efbb5-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efbb5-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="efbb5-119">-Confirm</span></span>
<span data-ttu-id="efbb5-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efbb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efbb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efbb5-121">-WhatIf</span></span>
<span data-ttu-id="efbb5-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="efbb5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efbb5-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="efbb5-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efbb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbb5-124">CommonParameters</span></span>
<span data-ttu-id="efbb5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efbb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbb5-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbb5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="efbb5-127">INPUTS</span></span>

### <span data-ttu-id="efbb5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="efbb5-128">System.String</span></span>

## <span data-ttu-id="efbb5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="efbb5-129">OUTPUTS</span></span>

### <span data-ttu-id="efbb5-130">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="efbb5-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="efbb5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="efbb5-131">NOTES</span></span>

## <span data-ttu-id="efbb5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efbb5-132">RELATED LINKS</span></span>

