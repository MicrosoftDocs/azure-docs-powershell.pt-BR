---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785589"
---
# <span data-ttu-id="704e3-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="704e3-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="704e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="704e3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="704e3-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="704e3-103">SYNTAX</span></span>

### <span data-ttu-id="704e3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="704e3-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="704e3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="704e3-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="704e3-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="704e3-106">DESCRIPTION</span></span>
<span data-ttu-id="704e3-107">O cmdlet **New-AzureRmWebAppBackup** cria um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="704e3-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="704e3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="704e3-108">EXAMPLES</span></span>

### <span data-ttu-id="704e3-109">1:</span><span class="sxs-lookup"><span data-stu-id="704e3-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="704e3-110">Cria um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="704e3-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="704e3-111">OS</span><span class="sxs-lookup"><span data-stu-id="704e3-111">PARAMETERS</span></span>

### <span data-ttu-id="704e3-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="704e3-112">-BackupName</span></span>
<span data-ttu-id="704e3-113">Nome do backup</span><span class="sxs-lookup"><span data-stu-id="704e3-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="704e3-114">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="704e3-114">-Databases</span></span>
<span data-ttu-id="704e3-115">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="704e3-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="704e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704e3-116">-DefaultProfile</span></span>
<span data-ttu-id="704e3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="704e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="704e3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="704e3-118">-Name</span></span>
<span data-ttu-id="704e3-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="704e3-119">WebApp Name</span></span>

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

### <span data-ttu-id="704e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="704e3-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="704e3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="704e3-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="704e3-122">-Slot</span></span>
<span data-ttu-id="704e3-123">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="704e3-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="704e3-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="704e3-124">-StorageAccountUrl</span></span>
<span data-ttu-id="704e3-125">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="704e3-125">Storage Account Url</span></span>

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

### <span data-ttu-id="704e3-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="704e3-126">-WebApp</span></span>
<span data-ttu-id="704e3-127">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="704e3-127">WebApp Object</span></span>

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

### <span data-ttu-id="704e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704e3-128">CommonParameters</span></span>
<span data-ttu-id="704e3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704e3-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704e3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704e3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="704e3-131">INPUTS</span></span>

### <span data-ttu-id="704e3-132">Instalação</span><span class="sxs-lookup"><span data-stu-id="704e3-132">Site</span></span>
<span data-ttu-id="704e3-133">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="704e3-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="704e3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="704e3-134">OUTPUTS</span></span>

### <span data-ttu-id="704e3-135">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="704e3-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="704e3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="704e3-136">NOTES</span></span>

## <span data-ttu-id="704e3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="704e3-137">RELATED LINKS</span></span>

