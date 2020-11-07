---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776120"
---
# <span data-ttu-id="14e48-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="14e48-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="14e48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14e48-102">SYNOPSIS</span></span>

## <span data-ttu-id="14e48-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14e48-103">SYNTAX</span></span>

### <span data-ttu-id="14e48-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="14e48-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14e48-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="14e48-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14e48-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14e48-106">DESCRIPTION</span></span>
<span data-ttu-id="14e48-107">O cmdlet **Get-AzWebAppBackup** Obtém o backup especificado de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="14e48-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="14e48-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14e48-108">EXAMPLES</span></span>

### <span data-ttu-id="14e48-109">1:</span><span class="sxs-lookup"><span data-stu-id="14e48-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="14e48-110">Esse comando obtém o backup com ID "12345" do aplicativo Web chamado WebAppStandard que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="14e48-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="14e48-111">OS</span><span class="sxs-lookup"><span data-stu-id="14e48-111">PARAMETERS</span></span>

### <span data-ttu-id="14e48-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="14e48-112">-BackupId</span></span>
<span data-ttu-id="14e48-113">ID de backup</span><span class="sxs-lookup"><span data-stu-id="14e48-113">Backup Id</span></span>

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

### <span data-ttu-id="14e48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e48-114">-DefaultProfile</span></span>
<span data-ttu-id="14e48-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14e48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14e48-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="14e48-116">-Name</span></span>
<span data-ttu-id="14e48-117">Nome do webapp</span><span class="sxs-lookup"><span data-stu-id="14e48-117">Webapp Name</span></span>

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

### <span data-ttu-id="14e48-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e48-118">-ResourceGroupName</span></span>
<span data-ttu-id="14e48-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="14e48-119">Resource Group Name</span></span>

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

### <span data-ttu-id="14e48-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="14e48-120">-Slot</span></span>
<span data-ttu-id="14e48-121">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="14e48-121">Slot Name</span></span>

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

### <span data-ttu-id="14e48-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="14e48-122">-WebApp</span></span>
<span data-ttu-id="14e48-123">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="14e48-123">Piped WebApp</span></span>

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

### <span data-ttu-id="14e48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e48-124">CommonParameters</span></span>
<span data-ttu-id="14e48-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e48-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14e48-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e48-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14e48-127">INPUTS</span></span>

### <span data-ttu-id="14e48-128">Instalação</span><span class="sxs-lookup"><span data-stu-id="14e48-128">Site</span></span>
<span data-ttu-id="14e48-129">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="14e48-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="14e48-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14e48-130">OUTPUTS</span></span>

### <span data-ttu-id="14e48-131">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="14e48-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="14e48-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14e48-132">NOTES</span></span>

## <span data-ttu-id="14e48-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14e48-133">RELATED LINKS</span></span>

