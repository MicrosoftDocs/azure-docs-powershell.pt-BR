---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430774"
---
# <span data-ttu-id="30821-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="30821-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="30821-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30821-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30821-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30821-103">SYNTAX</span></span>

### <span data-ttu-id="30821-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="30821-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="30821-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="30821-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="30821-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30821-106">DESCRIPTION</span></span>
<span data-ttu-id="30821-107">O cmdlet **Restore-AzureRmWebAppBackup** restaura um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="30821-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="30821-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30821-108">EXAMPLES</span></span>

### <span data-ttu-id="30821-109">1:</span><span class="sxs-lookup"><span data-stu-id="30821-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="30821-110">Restaura um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus no blob "myblob" localizado em https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="30821-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="30821-111">OS</span><span class="sxs-lookup"><span data-stu-id="30821-111">PARAMETERS</span></span>

### <span data-ttu-id="30821-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="30821-112">-AppServicePlan</span></span>
<span data-ttu-id="30821-113">O nome do plano de serviço de aplicativo para o aplicativo restaurado.</span><span class="sxs-lookup"><span data-stu-id="30821-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="30821-114">Se deixado vazio, o plano do serviço de aplicativo atual do aplicativo será usado.</span><span class="sxs-lookup"><span data-stu-id="30821-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="30821-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="30821-115">-BlobName</span></span>
<span data-ttu-id="30821-116">Nome do blob</span><span class="sxs-lookup"><span data-stu-id="30821-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-117">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="30821-117">-Databases</span></span>
<span data-ttu-id="30821-118">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="30821-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30821-119">-DefaultProfile</span></span>
<span data-ttu-id="30821-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30821-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30821-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="30821-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="30821-122">Opção ignorar nomes de host conflitantes</span><span class="sxs-lookup"><span data-stu-id="30821-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="30821-123">-Name</span></span>
<span data-ttu-id="30821-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="30821-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-125">-Substituir</span><span class="sxs-lookup"><span data-stu-id="30821-125">-Overwrite</span></span>
<span data-ttu-id="30821-126">Opção substituir</span><span class="sxs-lookup"><span data-stu-id="30821-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30821-127">-ResourceGroupName</span></span>
<span data-ttu-id="30821-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="30821-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="30821-129">-Slot</span></span>
<span data-ttu-id="30821-130">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="30821-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="30821-131">-StorageAccountUrl</span></span>
<span data-ttu-id="30821-132">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="30821-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="30821-133">-WebApp</span></span>
<span data-ttu-id="30821-134">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="30821-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30821-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30821-135">CommonParameters</span></span>
<span data-ttu-id="30821-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30821-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30821-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30821-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30821-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30821-138">INPUTS</span></span>

### <span data-ttu-id="30821-139">System. String</span><span class="sxs-lookup"><span data-stu-id="30821-139">System.String</span></span>

### <span data-ttu-id="30821-140">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="30821-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="30821-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30821-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="30821-142">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="30821-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="30821-143">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30821-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="30821-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30821-144">OUTPUTS</span></span>

### <span data-ttu-id="30821-145">System. void</span><span class="sxs-lookup"><span data-stu-id="30821-145">System.Void</span></span>

## <span data-ttu-id="30821-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30821-146">NOTES</span></span>

## <span data-ttu-id="30821-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30821-147">RELATED LINKS</span></span>
