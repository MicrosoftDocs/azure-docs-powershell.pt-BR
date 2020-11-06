---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/enable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 3ea06c98119775616cd8d5a4dbb8788dba4380bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602609"
---
# <span data-ttu-id="80755-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="80755-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="80755-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80755-102">SYNOPSIS</span></span>
<span data-ttu-id="80755-103">Habilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS especificado durante a ativação.</span><span class="sxs-lookup"><span data-stu-id="80755-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80755-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80755-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80755-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80755-105">DESCRIPTION</span></span>
<span data-ttu-id="80755-106">O cmdlet **Enable-AzureRmHDInsightOperationsManagementSuite** HABILITA o OMS (Operations Management Suite) em um cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="80755-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="80755-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80755-107">EXAMPLES</span></span>

### <span data-ttu-id="80755-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80755-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="80755-109">O serviço de gerenciamento de operações (OMS) será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS com a ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="80755-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="80755-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80755-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="80755-111">O serviço de gerenciamento de operações (OMS) será habilitado no cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS com a ID 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="80755-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="80755-112">OS</span><span class="sxs-lookup"><span data-stu-id="80755-112">PARAMETERS</span></span>

### <span data-ttu-id="80755-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80755-113">-DefaultProfile</span></span>
<span data-ttu-id="80755-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="80755-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80755-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="80755-115">-Name</span></span>
<span data-ttu-id="80755-116">O nome do cluster para habilitar o OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="80755-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="80755-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="80755-117">-PrimaryKey</span></span>
<span data-ttu-id="80755-118">A chave primária do espaço de trabalho do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="80755-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="80755-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80755-119">-ResourceGroupName</span></span>
<span data-ttu-id="80755-120">O grupo de recursos do cluster.</span><span class="sxs-lookup"><span data-stu-id="80755-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="80755-121">-Workspaceid</span><span class="sxs-lookup"><span data-stu-id="80755-121">-WorkspaceId</span></span>
<span data-ttu-id="80755-122">A ID do espaço de trabalho do OMS (Operations Management Suite).</span><span class="sxs-lookup"><span data-stu-id="80755-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

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

### <span data-ttu-id="80755-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="80755-123">-Confirm</span></span>
<span data-ttu-id="80755-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80755-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80755-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80755-125">-WhatIf</span></span>
<span data-ttu-id="80755-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80755-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80755-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80755-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80755-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80755-128">CommonParameters</span></span>
<span data-ttu-id="80755-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80755-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80755-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80755-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80755-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80755-131">INPUTS</span></span>

### <span data-ttu-id="80755-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80755-132">System.String</span></span>

## <span data-ttu-id="80755-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80755-133">OUTPUTS</span></span>

### <span data-ttu-id="80755-134">Microsoft. Azure. Management. HDInsight. Models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="80755-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="80755-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80755-135">NOTES</span></span>

## <span data-ttu-id="80755-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80755-136">RELATED LINKS</span></span>
