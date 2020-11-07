---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776098"
---
# <span data-ttu-id="00dbb-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="00dbb-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="00dbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00dbb-102">SYNOPSIS</span></span>

## <span data-ttu-id="00dbb-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00dbb-103">SYNTAX</span></span>

### <span data-ttu-id="00dbb-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="00dbb-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="00dbb-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="00dbb-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="00dbb-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00dbb-106">DESCRIPTION</span></span>
<span data-ttu-id="00dbb-107">O cmdlet **New-AzWebAppBackup** cria um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="00dbb-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="00dbb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00dbb-108">EXAMPLES</span></span>

### <span data-ttu-id="00dbb-109">1:</span><span class="sxs-lookup"><span data-stu-id="00dbb-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="00dbb-110">Cria um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="00dbb-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="00dbb-111">OS</span><span class="sxs-lookup"><span data-stu-id="00dbb-111">PARAMETERS</span></span>

### <span data-ttu-id="00dbb-112">-Backupname</span><span class="sxs-lookup"><span data-stu-id="00dbb-112">-BackupName</span></span>
<span data-ttu-id="00dbb-113">Nome do backup</span><span class="sxs-lookup"><span data-stu-id="00dbb-113">Backup Name</span></span>

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

### <span data-ttu-id="00dbb-114">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="00dbb-114">-Databases</span></span>
<span data-ttu-id="00dbb-115">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="00dbb-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="00dbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00dbb-116">-DefaultProfile</span></span>
<span data-ttu-id="00dbb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00dbb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00dbb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="00dbb-118">-Name</span></span>
<span data-ttu-id="00dbb-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="00dbb-119">WebApp Name</span></span>

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

### <span data-ttu-id="00dbb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00dbb-120">-ResourceGroupName</span></span>
<span data-ttu-id="00dbb-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="00dbb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="00dbb-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="00dbb-122">-Slot</span></span>
<span data-ttu-id="00dbb-123">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="00dbb-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="00dbb-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="00dbb-124">-StorageAccountUrl</span></span>
<span data-ttu-id="00dbb-125">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="00dbb-125">Storage Account Url</span></span>

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

### <span data-ttu-id="00dbb-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="00dbb-126">-WebApp</span></span>
<span data-ttu-id="00dbb-127">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="00dbb-127">WebApp Object</span></span>

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

### <span data-ttu-id="00dbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00dbb-128">CommonParameters</span></span>
<span data-ttu-id="00dbb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00dbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00dbb-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00dbb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00dbb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00dbb-131">INPUTS</span></span>

### <span data-ttu-id="00dbb-132">Instalação</span><span class="sxs-lookup"><span data-stu-id="00dbb-132">Site</span></span>
<span data-ttu-id="00dbb-133">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="00dbb-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="00dbb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00dbb-134">OUTPUTS</span></span>

### <span data-ttu-id="00dbb-135">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="00dbb-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="00dbb-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00dbb-136">NOTES</span></span>

## <span data-ttu-id="00dbb-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00dbb-137">RELATED LINKS</span></span>

