---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432155"
---
# <span data-ttu-id="35d85-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="35d85-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="35d85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35d85-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35d85-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35d85-103">SYNTAX</span></span>

### <span data-ttu-id="35d85-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="35d85-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35d85-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="35d85-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35d85-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35d85-106">DESCRIPTION</span></span>
<span data-ttu-id="35d85-107">O cmdlet **Get-AzureRmWebAppBackup** Obtém o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="35d85-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="35d85-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35d85-108">EXAMPLES</span></span>

### <span data-ttu-id="35d85-109">1:</span><span class="sxs-lookup"><span data-stu-id="35d85-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="35d85-110">Esse comando obtém o backup com ID "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="35d85-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="35d85-111">OS</span><span class="sxs-lookup"><span data-stu-id="35d85-111">PARAMETERS</span></span>

### <span data-ttu-id="35d85-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="35d85-112">-BackupId</span></span>
<span data-ttu-id="35d85-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="35d85-113">Backup Id</span></span>

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

### <span data-ttu-id="35d85-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="35d85-114">-Name</span></span>
<span data-ttu-id="35d85-115">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="35d85-115">Webapp Name</span></span>

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

### <span data-ttu-id="35d85-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d85-116">-ResourceGroupName</span></span>
<span data-ttu-id="35d85-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="35d85-117">Resource Group Name</span></span>

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

### <span data-ttu-id="35d85-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="35d85-118">-Slot</span></span>
<span data-ttu-id="35d85-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="35d85-119">Slot Name</span></span>

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

### <span data-ttu-id="35d85-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="35d85-120">-WebApp</span></span>
<span data-ttu-id="35d85-121">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="35d85-121">Piped WebApp</span></span>

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

### <span data-ttu-id="35d85-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d85-122">-DefaultProfile</span></span>
<span data-ttu-id="35d85-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35d85-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35d85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d85-124">CommonParameters</span></span>
<span data-ttu-id="35d85-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d85-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d85-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d85-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35d85-127">INPUTS</span></span>

### <span data-ttu-id="35d85-128">Instalação</span><span class="sxs-lookup"><span data-stu-id="35d85-128">Site</span></span>
<span data-ttu-id="35d85-129">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="35d85-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="35d85-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35d85-130">OUTPUTS</span></span>

### <span data-ttu-id="35d85-131">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="35d85-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="35d85-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35d85-132">NOTES</span></span>

## <span data-ttu-id="35d85-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35d85-133">RELATED LINKS</span></span>
