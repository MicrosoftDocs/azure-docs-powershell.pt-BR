---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 30f1581ddd4668fbe4d4d4b6d8c902f6aac929ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774408"
---
# <span data-ttu-id="0f793-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0f793-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="0f793-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f793-102">SYNOPSIS</span></span>

## <span data-ttu-id="0f793-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f793-103">SYNTAX</span></span>

### <span data-ttu-id="0f793-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0f793-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f793-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0f793-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f793-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f793-106">DESCRIPTION</span></span>
<span data-ttu-id="0f793-107">O cmdlet **Get-AzWebAppBackup** Obtém o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0f793-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="0f793-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f793-108">EXAMPLES</span></span>

### <span data-ttu-id="0f793-109">1:</span><span class="sxs-lookup"><span data-stu-id="0f793-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="0f793-110">Esse comando obtém o backup com ID "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="0f793-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0f793-111">OS</span><span class="sxs-lookup"><span data-stu-id="0f793-111">PARAMETERS</span></span>

### <span data-ttu-id="0f793-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="0f793-112">-BackupId</span></span>
<span data-ttu-id="0f793-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="0f793-113">Backup Id</span></span>

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

### <span data-ttu-id="0f793-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f793-114">-DefaultProfile</span></span>
<span data-ttu-id="0f793-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f793-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f793-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f793-116">-Name</span></span>
<span data-ttu-id="0f793-117">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="0f793-117">Webapp Name</span></span>

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

### <span data-ttu-id="0f793-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f793-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f793-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0f793-119">Resource Group Name</span></span>

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

### <span data-ttu-id="0f793-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="0f793-120">-Slot</span></span>
<span data-ttu-id="0f793-121">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="0f793-121">Slot Name</span></span>

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

### <span data-ttu-id="0f793-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0f793-122">-WebApp</span></span>
<span data-ttu-id="0f793-123">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="0f793-123">Piped WebApp</span></span>

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

### <span data-ttu-id="0f793-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f793-124">CommonParameters</span></span>
<span data-ttu-id="0f793-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f793-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f793-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f793-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f793-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f793-127">INPUTS</span></span>

### <span data-ttu-id="0f793-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0f793-128">System.String</span></span>

### <span data-ttu-id="0f793-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0f793-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0f793-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f793-130">OUTPUTS</span></span>

### <span data-ttu-id="0f793-131">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0f793-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="0f793-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f793-132">NOTES</span></span>

## <span data-ttu-id="0f793-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f793-133">RELATED LINKS</span></span>
