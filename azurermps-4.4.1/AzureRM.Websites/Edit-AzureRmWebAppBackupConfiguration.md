---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429017"
---
# <span data-ttu-id="ec6aa-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec6aa-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ec6aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec6aa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec6aa-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec6aa-103">SYNTAX</span></span>

### <span data-ttu-id="ec6aa-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ec6aa-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ec6aa-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ec6aa-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ec6aa-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec6aa-106">DESCRIPTION</span></span>
<span data-ttu-id="ec6aa-107">O cmdlet **Edit-AzureRmWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6aa-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ec6aa-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec6aa-108">EXAMPLES</span></span>

## <span data-ttu-id="ec6aa-109">OS</span><span class="sxs-lookup"><span data-stu-id="ec6aa-109">PARAMETERS</span></span>

### <span data-ttu-id="ec6aa-110">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="ec6aa-110">-Databases</span></span>
<span data-ttu-id="ec6aa-111">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ec6aa-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ec6aa-112">-FrequencyInterval</span></span>
<span data-ttu-id="ec6aa-113">Intervalo de frequência</span><span class="sxs-lookup"><span data-stu-id="ec6aa-113">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ec6aa-114">-FrequencyUnit</span></span>
<span data-ttu-id="ec6aa-115">Unidade de frequência</span><span class="sxs-lookup"><span data-stu-id="ec6aa-115">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="ec6aa-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ec6aa-117">Mantenha pelo menos uma opção de backup</span><span class="sxs-lookup"><span data-stu-id="ec6aa-117">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec6aa-118">-Name</span></span>
<span data-ttu-id="ec6aa-119">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ec6aa-119">WebApp Name</span></span>

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

### <span data-ttu-id="ec6aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec6aa-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ec6aa-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ec6aa-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ec6aa-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ec6aa-123">Período de retenção em dias</span><span class="sxs-lookup"><span data-stu-id="ec6aa-123">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="ec6aa-124">-Slot</span></span>
<span data-ttu-id="ec6aa-125">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ec6aa-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ec6aa-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ec6aa-126">-StartTime</span></span>
<span data-ttu-id="ec6aa-127">StartTime em UTC</span><span class="sxs-lookup"><span data-stu-id="ec6aa-127">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6aa-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ec6aa-128">-StorageAccountUrl</span></span>
<span data-ttu-id="ec6aa-129">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ec6aa-129">Storage Account Url</span></span>

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

### <span data-ttu-id="ec6aa-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec6aa-130">-WebApp</span></span>
<span data-ttu-id="ec6aa-131">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ec6aa-131">WebApp Object</span></span>

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

### <span data-ttu-id="ec6aa-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6aa-132">-DefaultProfile</span></span>
<span data-ttu-id="ec6aa-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec6aa-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec6aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6aa-134">CommonParameters</span></span>
<span data-ttu-id="ec6aa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6aa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec6aa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6aa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec6aa-137">INPUTS</span></span>

### <span data-ttu-id="ec6aa-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="ec6aa-138">Site</span></span>
<span data-ttu-id="ec6aa-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ec6aa-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ec6aa-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec6aa-140">OUTPUTS</span></span>

### <span data-ttu-id="ec6aa-141">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec6aa-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ec6aa-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec6aa-142">NOTES</span></span>

## <span data-ttu-id="ec6aa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec6aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ec6aa-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec6aa-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


