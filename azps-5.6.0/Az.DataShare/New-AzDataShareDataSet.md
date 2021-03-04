---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 12c0c4832d13e3e8637ab1cdb36a1f3fe3abb7d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887540"
---
# <span data-ttu-id="828d6-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="828d6-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="828d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828d6-102">SYNOPSIS</span></span>
<span data-ttu-id="828d6-103">Adiciona conjuntos de dados ao compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="828d6-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="828d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="828d6-104">SYNTAX</span></span>

### <span data-ttu-id="828d6-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="828d6-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="828d6-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="828d6-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="828d6-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="828d6-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="828d6-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="828d6-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="828d6-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="828d6-109">DESCRIPTION</span></span>
<span data-ttu-id="828d6-110">O cmdlet **New-AzDataShareDataSet** adiciona conjuntos de dados no compartilhamento de dados do azure da conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="828d6-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="828d6-111">Você pode adicionar conjuntos de dados do tipo Blob, ADLS Gen2 e ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="828d6-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="828d6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="828d6-112">EXAMPLES</span></span>

### <span data-ttu-id="828d6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="828d6-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="828d6-114">Este comando adiciona um conjuntos de dados chamado AdsDataSet do contêiner de blob de tipo ao compartilhamento de dados do azure AdsShare.</span><span class="sxs-lookup"><span data-stu-id="828d6-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="828d6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="828d6-115">PARAMETERS</span></span>

### <span data-ttu-id="828d6-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="828d6-116">-AccountName</span></span>
<span data-ttu-id="828d6-117">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="828d6-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="828d6-119">Caminho de pasta do ADLS gen1 de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-120">-Container</span><span class="sxs-lookup"><span data-stu-id="828d6-120">-Container</span></span>
<span data-ttu-id="828d6-121">Nome do contêiner da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="828d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828d6-122">-DefaultProfile</span></span>
<span data-ttu-id="828d6-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="828d6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828d6-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="828d6-124">-FileName</span></span>
<span data-ttu-id="828d6-125">Nome de arquivo do ADLS gen1 de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="828d6-126">-FilePath</span></span>
<span data-ttu-id="828d6-127">Caminho do arquivo de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-127">Azure storage file path</span></span>

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

### <span data-ttu-id="828d6-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="828d6-128">-FileSystem</span></span>
<span data-ttu-id="828d6-129">Nome do sistema de arquivos do Azure ADLS gen2</span><span class="sxs-lookup"><span data-stu-id="828d6-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="828d6-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="828d6-130">-FolderPath</span></span>
<span data-ttu-id="828d6-131">Caminho da pasta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="828d6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="828d6-132">-Name</span></span>
<span data-ttu-id="828d6-133">Nome do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828d6-134">-ResourceGroupName</span></span>
<span data-ttu-id="828d6-135">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="828d6-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="828d6-136">-ShareName</span></span>
<span data-ttu-id="828d6-137">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="828d6-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="828d6-139">ResourceId da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="828d6-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="828d6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="828d6-140">-Confirm</span></span>
<span data-ttu-id="828d6-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="828d6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="828d6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="828d6-142">-WhatIf</span></span>
<span data-ttu-id="828d6-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="828d6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828d6-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="828d6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="828d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828d6-145">CommonParameters</span></span>
<span data-ttu-id="828d6-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828d6-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="828d6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828d6-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="828d6-148">INPUTS</span></span>

### <span data-ttu-id="828d6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="828d6-149">System.String</span></span>

## <span data-ttu-id="828d6-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="828d6-150">OUTPUTS</span></span>

### <span data-ttu-id="828d6-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="828d6-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="828d6-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="828d6-152">NOTES</span></span>

## <span data-ttu-id="828d6-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="828d6-153">RELATED LINKS</span></span>
