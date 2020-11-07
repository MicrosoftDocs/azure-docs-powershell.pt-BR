---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 20d859782081991badab5fc9377fb69beb9550ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942903"
---
# <span data-ttu-id="f486f-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f486f-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="f486f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f486f-102">SYNOPSIS</span></span>

## <span data-ttu-id="f486f-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f486f-103">SYNTAX</span></span>

### <span data-ttu-id="f486f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f486f-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="f486f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f486f-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="f486f-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f486f-106">DESCRIPTION</span></span>
<span data-ttu-id="f486f-107">O cmdlet **Restore-AzWebAppBackup** restaura um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f486f-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="f486f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f486f-108">EXAMPLES</span></span>

### <span data-ttu-id="f486f-109">1:</span><span class="sxs-lookup"><span data-stu-id="f486f-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="f486f-110">Restaura um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus no blob "myblob" localizado em https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="f486f-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="f486f-111">OS</span><span class="sxs-lookup"><span data-stu-id="f486f-111">PARAMETERS</span></span>

### <span data-ttu-id="f486f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f486f-112">-AppServicePlan</span></span>
<span data-ttu-id="f486f-113">O nome do plano de serviço de aplicativo para o aplicativo restaurado.</span><span class="sxs-lookup"><span data-stu-id="f486f-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="f486f-114">Se deixado vazio, o plano do serviço de aplicativo atual do aplicativo será usado.</span><span class="sxs-lookup"><span data-stu-id="f486f-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="f486f-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="f486f-115">-BlobName</span></span>
<span data-ttu-id="f486f-116">Nome do blob</span><span class="sxs-lookup"><span data-stu-id="f486f-116">Blob Name</span></span>

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

### <span data-ttu-id="f486f-117">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="f486f-117">-Databases</span></span>
<span data-ttu-id="f486f-118">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f486f-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f486f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f486f-119">-DefaultProfile</span></span>
<span data-ttu-id="f486f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f486f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f486f-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="f486f-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="f486f-122">Opção ignorar nomes de host conflitantes</span><span class="sxs-lookup"><span data-stu-id="f486f-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="f486f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f486f-123">-Name</span></span>
<span data-ttu-id="f486f-124">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="f486f-124">WebApp Name</span></span>

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

### <span data-ttu-id="f486f-125">-Substituir</span><span class="sxs-lookup"><span data-stu-id="f486f-125">-Overwrite</span></span>
<span data-ttu-id="f486f-126">Opção substituir</span><span class="sxs-lookup"><span data-stu-id="f486f-126">Overwrite Option</span></span>

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

### <span data-ttu-id="f486f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f486f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f486f-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f486f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f486f-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="f486f-129">-Slot</span></span>
<span data-ttu-id="f486f-130">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="f486f-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f486f-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f486f-131">-StorageAccountUrl</span></span>
<span data-ttu-id="f486f-132">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f486f-132">Storage Account Url</span></span>

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

### <span data-ttu-id="f486f-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f486f-133">-WebApp</span></span>
<span data-ttu-id="f486f-134">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="f486f-134">WebApp Object</span></span>

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

### <span data-ttu-id="f486f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f486f-135">CommonParameters</span></span>
<span data-ttu-id="f486f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f486f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f486f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f486f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f486f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f486f-138">INPUTS</span></span>

### <span data-ttu-id="f486f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f486f-139">System.String</span></span>

### <span data-ttu-id="f486f-140">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f486f-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="f486f-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f486f-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f486f-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f486f-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f486f-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f486f-143">OUTPUTS</span></span>

### <span data-ttu-id="f486f-144">System. void</span><span class="sxs-lookup"><span data-stu-id="f486f-144">System.Void</span></span>

## <span data-ttu-id="f486f-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f486f-145">NOTES</span></span>

## <span data-ttu-id="f486f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f486f-146">RELATED LINKS</span></span>
