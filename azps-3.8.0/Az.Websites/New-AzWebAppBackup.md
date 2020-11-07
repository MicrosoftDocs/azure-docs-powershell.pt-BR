---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 36e8362551951dd068f8cafcd5430d069e8b5160
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940738"
---
# <span data-ttu-id="ad932-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ad932-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="ad932-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad932-102">SYNOPSIS</span></span>

## <span data-ttu-id="ad932-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad932-103">SYNTAX</span></span>

### <span data-ttu-id="ad932-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ad932-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ad932-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ad932-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ad932-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad932-106">DESCRIPTION</span></span>
<span data-ttu-id="ad932-107">O cmdlet **New-AzWebAppBackup** cria um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad932-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="ad932-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad932-108">EXAMPLES</span></span>

### <span data-ttu-id="ad932-109">1:</span><span class="sxs-lookup"><span data-stu-id="ad932-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="ad932-110">Cria um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ad932-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ad932-111">OS</span><span class="sxs-lookup"><span data-stu-id="ad932-111">PARAMETERS</span></span>

### <span data-ttu-id="ad932-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="ad932-112">-BackupName</span></span>
<span data-ttu-id="ad932-113">Nome do backup</span><span class="sxs-lookup"><span data-stu-id="ad932-113">Backup Name</span></span>

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

### <span data-ttu-id="ad932-114">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="ad932-114">-Databases</span></span>
<span data-ttu-id="ad932-115">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ad932-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ad932-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad932-116">-DefaultProfile</span></span>
<span data-ttu-id="ad932-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad932-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad932-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad932-118">-Name</span></span>
<span data-ttu-id="ad932-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ad932-119">WebApp Name</span></span>

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

### <span data-ttu-id="ad932-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad932-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad932-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ad932-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ad932-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad932-122">-Slot</span></span>
<span data-ttu-id="ad932-123">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ad932-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ad932-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ad932-124">-StorageAccountUrl</span></span>
<span data-ttu-id="ad932-125">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ad932-125">Storage Account Url</span></span>

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

### <span data-ttu-id="ad932-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad932-126">-WebApp</span></span>
<span data-ttu-id="ad932-127">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ad932-127">WebApp Object</span></span>

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

### <span data-ttu-id="ad932-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad932-128">CommonParameters</span></span>
<span data-ttu-id="ad932-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad932-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad932-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad932-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad932-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad932-131">INPUTS</span></span>

### <span data-ttu-id="ad932-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ad932-132">System.String</span></span>

### <span data-ttu-id="ad932-133">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ad932-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="ad932-134">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ad932-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="ad932-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad932-135">OUTPUTS</span></span>

### <span data-ttu-id="ad932-136">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ad932-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="ad932-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad932-137">NOTES</span></span>

## <span data-ttu-id="ad932-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad932-138">RELATED LINKS</span></span>
