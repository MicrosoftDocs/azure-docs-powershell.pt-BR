---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776132"
---
# <span data-ttu-id="ae3e6-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3e6-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ae3e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae3e6-102">SYNOPSIS</span></span>

## <span data-ttu-id="ae3e6-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae3e6-103">SYNTAX</span></span>

### <span data-ttu-id="ae3e6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ae3e6-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ae3e6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ae3e6-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ae3e6-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae3e6-106">DESCRIPTION</span></span>
<span data-ttu-id="ae3e6-107">O cmdlet **Edit-AzWebAppBackupConfiguration** edita o backup de configuração atual para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ae3e6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae3e6-108">EXAMPLES</span></span>

## <span data-ttu-id="ae3e6-109">OS</span><span class="sxs-lookup"><span data-stu-id="ae3e6-109">PARAMETERS</span></span>

### <span data-ttu-id="ae3e6-110">-Bancos de dados</span><span class="sxs-lookup"><span data-stu-id="ae3e6-110">-Databases</span></span>
<span data-ttu-id="ae3e6-111">Bancos de dados do tipo DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ae3e6-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ae3e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3e6-112">-DefaultProfile</span></span>
<span data-ttu-id="ae3e6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae3e6-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ae3e6-114">-FrequencyInterval</span></span>
<span data-ttu-id="ae3e6-115">Intervalo de frequência</span><span class="sxs-lookup"><span data-stu-id="ae3e6-115">Frequency Interval</span></span>

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

### <span data-ttu-id="ae3e6-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ae3e6-116">-FrequencyUnit</span></span>
<span data-ttu-id="ae3e6-117">Unidade de frequência</span><span class="sxs-lookup"><span data-stu-id="ae3e6-117">Frequency Unit</span></span>

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

### <span data-ttu-id="ae3e6-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="ae3e6-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ae3e6-119">Mantenha pelo menos uma opção de backup</span><span class="sxs-lookup"><span data-stu-id="ae3e6-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="ae3e6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae3e6-120">-Name</span></span>
<span data-ttu-id="ae3e6-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ae3e6-121">WebApp Name</span></span>

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

### <span data-ttu-id="ae3e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae3e6-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ae3e6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ae3e6-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ae3e6-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ae3e6-125">Período de retenção em dias</span><span class="sxs-lookup"><span data-stu-id="ae3e6-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="ae3e6-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae3e6-126">-Slot</span></span>
<span data-ttu-id="ae3e6-127">Nome do slot do WebApp</span><span class="sxs-lookup"><span data-stu-id="ae3e6-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ae3e6-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ae3e6-128">-StartTime</span></span>
<span data-ttu-id="ae3e6-129">StartTime em UTC</span><span class="sxs-lookup"><span data-stu-id="ae3e6-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="ae3e6-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ae3e6-130">-StorageAccountUrl</span></span>
<span data-ttu-id="ae3e6-131">URL da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ae3e6-131">Storage Account Url</span></span>

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

### <span data-ttu-id="ae3e6-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae3e6-132">-WebApp</span></span>
<span data-ttu-id="ae3e6-133">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="ae3e6-133">WebApp Object</span></span>

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

### <span data-ttu-id="ae3e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3e6-134">CommonParameters</span></span>
<span data-ttu-id="ae3e6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3e6-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3e6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3e6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae3e6-137">INPUTS</span></span>

### <span data-ttu-id="ae3e6-138">Instalação</span><span class="sxs-lookup"><span data-stu-id="ae3e6-138">Site</span></span>
<span data-ttu-id="ae3e6-139">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ae3e6-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ae3e6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae3e6-140">OUTPUTS</span></span>

### <span data-ttu-id="ae3e6-141">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3e6-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ae3e6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae3e6-142">NOTES</span></span>

## <span data-ttu-id="ae3e6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae3e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="ae3e6-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae3e6-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


