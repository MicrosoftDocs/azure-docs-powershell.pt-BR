---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4319a2637b2dbb008056a6b369ace539b889cd37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774381"
---
# <span data-ttu-id="ce91c-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce91c-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ce91c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce91c-102">SYNOPSIS</span></span>

## <span data-ttu-id="ce91c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce91c-103">SYNTAX</span></span>

### <span data-ttu-id="ce91c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ce91c-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ce91c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ce91c-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ce91c-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce91c-106">DESCRIPTION</span></span>
<span data-ttu-id="ce91c-107">O cmdlet **Edit-AzWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce91c-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ce91c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce91c-108">EXAMPLES</span></span>

## <span data-ttu-id="ce91c-109">OS</span><span class="sxs-lookup"><span data-stu-id="ce91c-109">PARAMETERS</span></span>

### <span data-ttu-id="ce91c-110">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="ce91c-110">-Databases</span></span>
<span data-ttu-id="ce91c-111">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ce91c-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ce91c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce91c-112">-DefaultProfile</span></span>
<span data-ttu-id="ce91c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce91c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce91c-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ce91c-114">-FrequencyInterval</span></span>
<span data-ttu-id="ce91c-115">Intervalo de frequência</span><span class="sxs-lookup"><span data-stu-id="ce91c-115">Frequency Interval</span></span>

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

### <span data-ttu-id="ce91c-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ce91c-116">-FrequencyUnit</span></span>
<span data-ttu-id="ce91c-117">Unidade de frequência</span><span class="sxs-lookup"><span data-stu-id="ce91c-117">Frequency Unit</span></span>

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

### <span data-ttu-id="ce91c-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="ce91c-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ce91c-119">Mantenha pelo menos uma opção de backup</span><span class="sxs-lookup"><span data-stu-id="ce91c-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="ce91c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce91c-120">-Name</span></span>
<span data-ttu-id="ce91c-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ce91c-121">WebApp Name</span></span>

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

### <span data-ttu-id="ce91c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce91c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce91c-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ce91c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ce91c-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ce91c-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ce91c-125">Período de retenção em dias</span><span class="sxs-lookup"><span data-stu-id="ce91c-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="ce91c-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="ce91c-126">-Slot</span></span>
<span data-ttu-id="ce91c-127">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ce91c-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ce91c-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce91c-128">-StartTime</span></span>
<span data-ttu-id="ce91c-129">StartTime em UTC</span><span class="sxs-lookup"><span data-stu-id="ce91c-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="ce91c-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ce91c-130">-StorageAccountUrl</span></span>
<span data-ttu-id="ce91c-131">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ce91c-131">Storage Account Url</span></span>

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

### <span data-ttu-id="ce91c-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ce91c-132">-WebApp</span></span>
<span data-ttu-id="ce91c-133">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ce91c-133">WebApp Object</span></span>

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

### <span data-ttu-id="ce91c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce91c-134">CommonParameters</span></span>
<span data-ttu-id="ce91c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce91c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce91c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce91c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce91c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce91c-137">INPUTS</span></span>

### <span data-ttu-id="ce91c-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ce91c-138">System.Int32</span></span>

### <span data-ttu-id="ce91c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ce91c-139">System.String</span></span>

### <span data-ttu-id="ce91c-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ce91c-140">System.DateTime</span></span>

### <span data-ttu-id="ce91c-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce91c-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ce91c-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ce91c-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="ce91c-143">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ce91c-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="ce91c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce91c-144">OUTPUTS</span></span>

### <span data-ttu-id="ce91c-145">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce91c-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ce91c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce91c-146">NOTES</span></span>

## <span data-ttu-id="ce91c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce91c-147">RELATED LINKS</span></span>

[<span data-ttu-id="ce91c-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce91c-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


