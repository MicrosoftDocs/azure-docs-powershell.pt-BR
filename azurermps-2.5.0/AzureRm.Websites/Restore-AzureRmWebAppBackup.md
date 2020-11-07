---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786206"
---
# <span data-ttu-id="a19d5-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="a19d5-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="a19d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a19d5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a19d5-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a19d5-103">SYNTAX</span></span>

### <span data-ttu-id="a19d5-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a19d5-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="a19d5-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a19d5-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="a19d5-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a19d5-106">DESCRIPTION</span></span>
<span data-ttu-id="a19d5-107">O cmdlet **Restore-AzureRmWebAppBackup** restaura um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a19d5-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="a19d5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a19d5-108">EXAMPLES</span></span>

### <span data-ttu-id="a19d5-109">1:</span><span class="sxs-lookup"><span data-stu-id="a19d5-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="a19d5-110">Restaura um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus no blob "myblob" localizado em https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="a19d5-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="a19d5-111">OS</span><span class="sxs-lookup"><span data-stu-id="a19d5-111">PARAMETERS</span></span>

### <span data-ttu-id="a19d5-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a19d5-112">-AppServicePlan</span></span>
<span data-ttu-id="a19d5-113">O nome do plano de serviço de aplicativo para o aplicativo restaurado.</span><span class="sxs-lookup"><span data-stu-id="a19d5-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="a19d5-114">Se deixado vazio, o plano do serviço de aplicativo atual do aplicativo será usado.</span><span class="sxs-lookup"><span data-stu-id="a19d5-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="a19d5-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="a19d5-115">-BlobName</span></span>
<span data-ttu-id="a19d5-116">Nome do blob</span><span class="sxs-lookup"><span data-stu-id="a19d5-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-117">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="a19d5-117">-Databases</span></span>
<span data-ttu-id="a19d5-118">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="a19d5-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19d5-119">-DefaultProfile</span></span>
<span data-ttu-id="a19d5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a19d5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a19d5-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="a19d5-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="a19d5-122">Opção ignorar nomes de host conflitantes</span><span class="sxs-lookup"><span data-stu-id="a19d5-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a19d5-123">-Name</span></span>
<span data-ttu-id="a19d5-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="a19d5-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-125">-Substituir</span><span class="sxs-lookup"><span data-stu-id="a19d5-125">-Overwrite</span></span>
<span data-ttu-id="a19d5-126">Opção substituir</span><span class="sxs-lookup"><span data-stu-id="a19d5-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="a19d5-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a19d5-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="a19d5-129">-Slot</span></span>
<span data-ttu-id="a19d5-130">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="a19d5-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="a19d5-131">-StorageAccountUrl</span></span>
<span data-ttu-id="a19d5-132">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a19d5-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a19d5-133">-WebApp</span></span>
<span data-ttu-id="a19d5-134">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="a19d5-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a19d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19d5-135">CommonParameters</span></span>
<span data-ttu-id="a19d5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19d5-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19d5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19d5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a19d5-138">INPUTS</span></span>

### <span data-ttu-id="a19d5-139">Instalação</span><span class="sxs-lookup"><span data-stu-id="a19d5-139">Site</span></span>
<span data-ttu-id="a19d5-140">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a19d5-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a19d5-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a19d5-141">OUTPUTS</span></span>

## <span data-ttu-id="a19d5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a19d5-142">NOTES</span></span>

## <span data-ttu-id="a19d5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a19d5-143">RELATED LINKS</span></span>

