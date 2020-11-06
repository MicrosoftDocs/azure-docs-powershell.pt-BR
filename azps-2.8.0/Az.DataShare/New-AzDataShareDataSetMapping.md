---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 0d7e1d62db25b70423ac40bc53ae0ff68f609eb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596705"
---
# <span data-ttu-id="e0644-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e0644-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="e0644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0644-102">SYNOPSIS</span></span>
<span data-ttu-id="e0644-103">Cria um mapeamento de conjuntos de dados para a assinatura de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e0644-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="e0644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0644-104">SYNTAX</span></span>

### <span data-ttu-id="e0644-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0644-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0644-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="e0644-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0644-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0644-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0644-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0644-108">DESCRIPTION</span></span>
<span data-ttu-id="e0644-109">O cmdlet **New-AzDataShareDataSetMapping** cria um mapeamento de conjuntos de dados entre os conjuntos de dados de origem e a conta de armazenamento do coletor na assinatura do compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e0644-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="e0644-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0644-110">EXAMPLES</span></span>

### <span data-ttu-id="e0644-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0644-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="e0644-112">Esse comando cria um mapeamento de conjunto de dados AdsDataSetMapping para a conta de armazenamento AdsStorage para a assinatura de compartilhamento AdsShareSubscription em WikiAdsAccount de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="e0644-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="e0644-113">OS</span><span class="sxs-lookup"><span data-stu-id="e0644-113">PARAMETERS</span></span>

### <span data-ttu-id="e0644-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e0644-114">-AccountName</span></span>
<span data-ttu-id="e0644-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-116">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="e0644-116">-Container</span></span>
<span data-ttu-id="e0644-117">Nome do contêiner da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-118">-DataSetid</span><span class="sxs-lookup"><span data-stu-id="e0644-118">-DataSetId</span></span>
<span data-ttu-id="e0644-119">ID do conjunto de dados do consumidor</span><span class="sxs-lookup"><span data-stu-id="e0644-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0644-120">-DefaultProfile</span></span>
<span data-ttu-id="e0644-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0644-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0644-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e0644-122">-FilePath</span></span>
<span data-ttu-id="e0644-123">Caminho do arquivo de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="e0644-124">-FileSystem</span></span>
<span data-ttu-id="e0644-125">Nome do sistema de arquivos Gen2 do ADLS</span><span class="sxs-lookup"><span data-stu-id="e0644-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="e0644-126">-FolderPath</span></span>
<span data-ttu-id="e0644-127">Caminho da pasta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0644-128">-Name</span></span>
<span data-ttu-id="e0644-129">Nome do mapeamento do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0644-130">-ResourceGroupName</span></span>
<span data-ttu-id="e0644-131">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="e0644-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e0644-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="e0644-133">Nome da assinatura do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e0644-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="e0644-135">ResourceId da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="e0644-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0644-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0644-136">-Confirm</span></span>
<span data-ttu-id="e0644-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0644-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0644-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0644-138">-WhatIf</span></span>
<span data-ttu-id="e0644-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0644-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0644-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0644-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0644-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0644-141">CommonParameters</span></span>
<span data-ttu-id="e0644-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0644-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0644-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0644-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0644-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0644-144">INPUTS</span></span>

### <span data-ttu-id="e0644-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e0644-145">System.String</span></span>

## <span data-ttu-id="e0644-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0644-146">OUTPUTS</span></span>

### <span data-ttu-id="e0644-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e0644-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="e0644-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0644-148">NOTES</span></span>

## <span data-ttu-id="e0644-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0644-149">RELATED LINKS</span></span>
