---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610689"
---
# <span data-ttu-id="8e2af-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8e2af-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="8e2af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e2af-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e2af-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e2af-103">SYNTAX</span></span>

### <span data-ttu-id="8e2af-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8e2af-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="8e2af-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8e2af-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="8e2af-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e2af-106">DESCRIPTION</span></span>
<span data-ttu-id="8e2af-107">O cmdlet **New-AzureRmWebAppBackup** cria um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8e2af-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="8e2af-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e2af-108">EXAMPLES</span></span>

### <span data-ttu-id="8e2af-109">1:</span><span class="sxs-lookup"><span data-stu-id="8e2af-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="8e2af-110">Cria um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="8e2af-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="8e2af-111">OS</span><span class="sxs-lookup"><span data-stu-id="8e2af-111">PARAMETERS</span></span>

### <span data-ttu-id="8e2af-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="8e2af-112">-BackupName</span></span>
<span data-ttu-id="8e2af-113">Nome do backup</span><span class="sxs-lookup"><span data-stu-id="8e2af-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2af-114">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="8e2af-114">-Databases</span></span>
<span data-ttu-id="8e2af-115">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="8e2af-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="8e2af-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e2af-116">-Name</span></span>
<span data-ttu-id="8e2af-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8e2af-117">WebApp Name</span></span>

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

### <span data-ttu-id="8e2af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2af-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e2af-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8e2af-119">Resource Group Name</span></span>

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

### <span data-ttu-id="8e2af-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="8e2af-120">-Slot</span></span>
<span data-ttu-id="8e2af-121">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="8e2af-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8e2af-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="8e2af-122">-StorageAccountUrl</span></span>
<span data-ttu-id="8e2af-123">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8e2af-123">Storage Account Url</span></span>

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

### <span data-ttu-id="8e2af-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8e2af-124">-WebApp</span></span>
<span data-ttu-id="8e2af-125">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="8e2af-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2af-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2af-126">-DefaultProfile</span></span>
<span data-ttu-id="8e2af-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2af-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2af-128">CommonParameters</span></span>
<span data-ttu-id="8e2af-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2af-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2af-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e2af-131">INPUTS</span></span>

### <span data-ttu-id="8e2af-132">Instalação</span><span class="sxs-lookup"><span data-stu-id="8e2af-132">Site</span></span>
<span data-ttu-id="8e2af-133">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="8e2af-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8e2af-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e2af-134">OUTPUTS</span></span>

### <span data-ttu-id="8e2af-135">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8e2af-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="8e2af-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e2af-136">NOTES</span></span>

## <span data-ttu-id="8e2af-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e2af-137">RELATED LINKS</span></span>

