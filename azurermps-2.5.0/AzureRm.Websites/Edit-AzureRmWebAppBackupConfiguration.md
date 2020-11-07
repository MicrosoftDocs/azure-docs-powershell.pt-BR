---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 9a90e56909de016bb388be1a43f5b41c8e47e9e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785419"
---
# <span data-ttu-id="6411e-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6411e-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6411e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6411e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6411e-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6411e-103">SYNTAX</span></span>

### <span data-ttu-id="6411e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6411e-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="6411e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6411e-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="6411e-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6411e-106">DESCRIPTION</span></span>
<span data-ttu-id="6411e-107">O cmdlet **Edit-AzureRmWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="6411e-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="6411e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6411e-108">EXAMPLES</span></span>

## <span data-ttu-id="6411e-109">OS</span><span class="sxs-lookup"><span data-stu-id="6411e-109">PARAMETERS</span></span>

### <span data-ttu-id="6411e-110">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="6411e-110">-Databases</span></span>
<span data-ttu-id="6411e-111">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="6411e-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="6411e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6411e-112">-DefaultProfile</span></span>
<span data-ttu-id="6411e-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6411e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6411e-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="6411e-114">-FrequencyInterval</span></span>
<span data-ttu-id="6411e-115">Intervalo de frequência</span><span class="sxs-lookup"><span data-stu-id="6411e-115">Frequency Interval</span></span>

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

### <span data-ttu-id="6411e-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="6411e-116">-FrequencyUnit</span></span>
<span data-ttu-id="6411e-117">Unidade de frequência</span><span class="sxs-lookup"><span data-stu-id="6411e-117">Frequency Unit</span></span>

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

### <span data-ttu-id="6411e-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="6411e-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="6411e-119">Mantenha pelo menos uma opção de backup</span><span class="sxs-lookup"><span data-stu-id="6411e-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="6411e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6411e-120">-Name</span></span>
<span data-ttu-id="6411e-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6411e-121">WebApp Name</span></span>

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

### <span data-ttu-id="6411e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6411e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6411e-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6411e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6411e-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6411e-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="6411e-125">Período de retenção em dias</span><span class="sxs-lookup"><span data-stu-id="6411e-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="6411e-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="6411e-126">-Slot</span></span>
<span data-ttu-id="6411e-127">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="6411e-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6411e-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6411e-128">-StartTime</span></span>
<span data-ttu-id="6411e-129">StartTime em UTC</span><span class="sxs-lookup"><span data-stu-id="6411e-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="6411e-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="6411e-130">-StorageAccountUrl</span></span>
<span data-ttu-id="6411e-131">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="6411e-131">Storage Account Url</span></span>

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

### <span data-ttu-id="6411e-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6411e-132">-WebApp</span></span>
<span data-ttu-id="6411e-133">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="6411e-133">WebApp Object</span></span>

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

### <span data-ttu-id="6411e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6411e-134">CommonParameters</span></span>
<span data-ttu-id="6411e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6411e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6411e-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6411e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6411e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6411e-137">INPUTS</span></span>

### <span data-ttu-id="6411e-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="6411e-138">Site</span></span>
<span data-ttu-id="6411e-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6411e-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6411e-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6411e-140">OUTPUTS</span></span>

### <span data-ttu-id="6411e-141">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6411e-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6411e-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6411e-142">NOTES</span></span>

## <span data-ttu-id="6411e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6411e-143">RELATED LINKS</span></span>

[<span data-ttu-id="6411e-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6411e-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


