---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 9478e4892d4d7effdf37b7312f82348a2e8ea03a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596712"
---
# <span data-ttu-id="4f9a3-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4f9a3-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="4f9a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9a3-103">Adiciona conjuntos de dados ao compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="4f9a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f9a3-104">SYNTAX</span></span>

### <span data-ttu-id="4f9a3-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f9a3-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f9a3-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="4f9a3-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f9a3-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f9a3-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f9a3-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f9a3-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f9a3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f9a3-109">DESCRIPTION</span></span>
<span data-ttu-id="4f9a3-110">O cmdlet **New-AzDataShareDataSet** adiciona conjuntos de dados no compartilhamento de dados do Azure da conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="4f9a3-111">Você pode adicionar conjuntos de dados do tipo BLOB, ADLS Gen2 e ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="4f9a3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f9a3-112">EXAMPLES</span></span>

### <span data-ttu-id="4f9a3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f9a3-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="4f9a3-114">Esse comando adiciona um conjunto de dados chamado AdsDataSet do contêiner de blob de tipo ao Azure data share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="4f9a3-115">OS</span><span class="sxs-lookup"><span data-stu-id="4f9a3-115">PARAMETERS</span></span>

### <span data-ttu-id="4f9a3-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f9a3-116">-AccountName</span></span>
<span data-ttu-id="4f9a3-117">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-117">Azure data share account name</span></span>

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

### <span data-ttu-id="4f9a3-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="4f9a3-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="4f9a3-119">Caminho da pasta Gen1 do armazenamento do ADLS</span><span class="sxs-lookup"><span data-stu-id="4f9a3-119">Azure storage ADLS gen1 folder path</span></span>

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

### <span data-ttu-id="4f9a3-120">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="4f9a3-120">-Container</span></span>
<span data-ttu-id="4f9a3-121">Nome do contêiner da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="4f9a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9a3-122">-DefaultProfile</span></span>
<span data-ttu-id="4f9a3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f9a3-124">-Nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="4f9a3-124">-FileName</span></span>
<span data-ttu-id="4f9a3-125">Nome de arquivo do ADLS Gen1 de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-125">Azure storage ADLS gen1 file name</span></span>

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

### <span data-ttu-id="4f9a3-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="4f9a3-126">-FilePath</span></span>
<span data-ttu-id="4f9a3-127">Caminho do arquivo de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-127">Azure storage file path</span></span>

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

### <span data-ttu-id="4f9a3-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="4f9a3-128">-FileSystem</span></span>
<span data-ttu-id="4f9a3-129">Nome do sistema de arquivos Gen2 do ADLS</span><span class="sxs-lookup"><span data-stu-id="4f9a3-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="4f9a3-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="4f9a3-130">-FolderPath</span></span>
<span data-ttu-id="4f9a3-131">Caminho da pasta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="4f9a3-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f9a3-132">-Name</span></span>
<span data-ttu-id="4f9a3-133">Nome do conjunto de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-133">Azure data set name</span></span>

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

### <span data-ttu-id="4f9a3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9a3-134">-ResourceGroupName</span></span>
<span data-ttu-id="4f9a3-135">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="4f9a3-135">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4f9a3-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4f9a3-136">-ShareName</span></span>
<span data-ttu-id="4f9a3-137">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-137">Azure data share name</span></span>

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

### <span data-ttu-id="4f9a3-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4f9a3-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="4f9a3-139">ResourceId da conta de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4f9a3-139">Azure storage account resourceId</span></span>

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

### <span data-ttu-id="4f9a3-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4f9a3-140">-Confirm</span></span>
<span data-ttu-id="4f9a3-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9a3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9a3-142">-WhatIf</span></span>
<span data-ttu-id="4f9a3-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f9a3-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9a3-145">CommonParameters</span></span>
<span data-ttu-id="4f9a3-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f9a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9a3-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f9a3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9a3-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f9a3-148">INPUTS</span></span>

### <span data-ttu-id="4f9a3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4f9a3-149">System.String</span></span>

## <span data-ttu-id="4f9a3-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f9a3-150">OUTPUTS</span></span>

### <span data-ttu-id="4f9a3-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4f9a3-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="4f9a3-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f9a3-152">NOTES</span></span>

## <span data-ttu-id="4f9a3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f9a3-153">RELATED LINKS</span></span>
