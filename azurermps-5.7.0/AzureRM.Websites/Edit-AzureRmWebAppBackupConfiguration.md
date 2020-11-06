---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432852"
---
# <span data-ttu-id="494e2-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="494e2-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="494e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="494e2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="494e2-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="494e2-103">SYNTAX</span></span>

### <span data-ttu-id="494e2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="494e2-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="494e2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="494e2-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="494e2-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="494e2-106">DESCRIPTION</span></span>
<span data-ttu-id="494e2-107">O cmdlet **Edit-AzureRmWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="494e2-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="494e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="494e2-108">EXAMPLES</span></span>

## <span data-ttu-id="494e2-109">OS</span><span class="sxs-lookup"><span data-stu-id="494e2-109">PARAMETERS</span></span>

### <span data-ttu-id="494e2-110">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="494e2-110">-Databases</span></span>
<span data-ttu-id="494e2-111">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="494e2-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="494e2-112">-DefaultProfile</span></span>
<span data-ttu-id="494e2-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="494e2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="494e2-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="494e2-114">-FrequencyInterval</span></span>
<span data-ttu-id="494e2-115">Intervalo de frequência</span><span class="sxs-lookup"><span data-stu-id="494e2-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="494e2-116">-FrequencyUnit</span></span>
<span data-ttu-id="494e2-117">Unidade de frequência</span><span class="sxs-lookup"><span data-stu-id="494e2-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="494e2-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="494e2-119">Mantenha pelo menos uma opção de backup</span><span class="sxs-lookup"><span data-stu-id="494e2-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="494e2-120">-Name</span></span>
<span data-ttu-id="494e2-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="494e2-121">WebApp Name</span></span>

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

### <span data-ttu-id="494e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="494e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="494e2-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="494e2-123">Resource Group Name</span></span>

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

### <span data-ttu-id="494e2-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="494e2-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="494e2-125">Período de retenção em dias</span><span class="sxs-lookup"><span data-stu-id="494e2-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="494e2-126">-Slot</span></span>
<span data-ttu-id="494e2-127">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="494e2-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="494e2-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="494e2-128">-StartTime</span></span>
<span data-ttu-id="494e2-129">StartTime em UTC</span><span class="sxs-lookup"><span data-stu-id="494e2-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="494e2-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="494e2-130">-StorageAccountUrl</span></span>
<span data-ttu-id="494e2-131">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="494e2-131">Storage Account Url</span></span>

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

### <span data-ttu-id="494e2-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="494e2-132">-WebApp</span></span>
<span data-ttu-id="494e2-133">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="494e2-133">WebApp Object</span></span>

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

### <span data-ttu-id="494e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="494e2-134">CommonParameters</span></span>
<span data-ttu-id="494e2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="494e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="494e2-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="494e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="494e2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="494e2-137">INPUTS</span></span>

### <span data-ttu-id="494e2-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="494e2-138">Site</span></span>
<span data-ttu-id="494e2-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="494e2-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="494e2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="494e2-140">OUTPUTS</span></span>

### <span data-ttu-id="494e2-141">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="494e2-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="494e2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="494e2-142">NOTES</span></span>

## <span data-ttu-id="494e2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="494e2-143">RELATED LINKS</span></span>

[<span data-ttu-id="494e2-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="494e2-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


