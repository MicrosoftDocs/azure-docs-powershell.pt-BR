---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432842"
---
# <span data-ttu-id="85d07-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="85d07-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="85d07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85d07-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85d07-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85d07-103">SYNTAX</span></span>

### <span data-ttu-id="85d07-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="85d07-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="85d07-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="85d07-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="85d07-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85d07-106">DESCRIPTION</span></span>
<span data-ttu-id="85d07-107">O cmdlet **Restore-AzureRmWebAppBackup** restaura um backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="85d07-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="85d07-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85d07-108">EXAMPLES</span></span>

### <span data-ttu-id="85d07-109">1:</span><span class="sxs-lookup"><span data-stu-id="85d07-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="85d07-110">Restaura um backup do aplicativo especificado ContosoWebApp que está dentro do grupo padrão do grupo de recursos-Web-Westus no blob "myblob" localizado em https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="85d07-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="85d07-111">OS</span><span class="sxs-lookup"><span data-stu-id="85d07-111">PARAMETERS</span></span>

### <span data-ttu-id="85d07-112">-Blobname</span><span class="sxs-lookup"><span data-stu-id="85d07-112">-BlobName</span></span>
<span data-ttu-id="85d07-113">Nome do blob</span><span class="sxs-lookup"><span data-stu-id="85d07-113">Blob Name</span></span>

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

### <span data-ttu-id="85d07-114">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="85d07-114">-Databases</span></span>
<span data-ttu-id="85d07-115">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="85d07-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="85d07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85d07-116">-DefaultProfile</span></span>
<span data-ttu-id="85d07-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85d07-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85d07-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="85d07-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="85d07-119">Opção ignorar nomes de host conflitantes</span><span class="sxs-lookup"><span data-stu-id="85d07-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="85d07-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="85d07-120">-Name</span></span>
<span data-ttu-id="85d07-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="85d07-121">WebApp Name</span></span>

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

### <span data-ttu-id="85d07-122">-Substituir</span><span class="sxs-lookup"><span data-stu-id="85d07-122">-Overwrite</span></span>
<span data-ttu-id="85d07-123">Opção substituir</span><span class="sxs-lookup"><span data-stu-id="85d07-123">Overwrite Option</span></span>

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

### <span data-ttu-id="85d07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85d07-124">-ResourceGroupName</span></span>
<span data-ttu-id="85d07-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="85d07-125">Resource Group Name</span></span>

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

### <span data-ttu-id="85d07-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="85d07-126">-Slot</span></span>
<span data-ttu-id="85d07-127">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="85d07-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="85d07-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="85d07-128">-StorageAccountUrl</span></span>
<span data-ttu-id="85d07-129">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="85d07-129">Storage Account Url</span></span>

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

### <span data-ttu-id="85d07-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="85d07-130">-WebApp</span></span>
<span data-ttu-id="85d07-131">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="85d07-131">WebApp Object</span></span>

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

### <span data-ttu-id="85d07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85d07-132">CommonParameters</span></span>
<span data-ttu-id="85d07-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85d07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85d07-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85d07-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85d07-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85d07-135">INPUTS</span></span>

### <span data-ttu-id="85d07-136">Instalação</span><span class="sxs-lookup"><span data-stu-id="85d07-136">Site</span></span>
<span data-ttu-id="85d07-137">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="85d07-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="85d07-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85d07-138">OUTPUTS</span></span>

## <span data-ttu-id="85d07-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85d07-139">NOTES</span></span>

## <span data-ttu-id="85d07-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85d07-140">RELATED LINKS</span></span>

