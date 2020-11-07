---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785412"
---
# <span data-ttu-id="cbae5-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="cbae5-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="cbae5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbae5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbae5-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbae5-103">SYNTAX</span></span>

### <span data-ttu-id="cbae5-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cbae5-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbae5-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cbae5-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbae5-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbae5-106">DESCRIPTION</span></span>
<span data-ttu-id="cbae5-107">O cmdlet **Get-AzureRmWebAppBackupList** Obtém uma lista de backups para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae5-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="cbae5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbae5-108">EXAMPLES</span></span>

### <span data-ttu-id="cbae5-109">1:</span><span class="sxs-lookup"><span data-stu-id="cbae5-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="cbae5-110">Esse comando retorna uma lista de backup relacionada a WebApp WebAppStandard associada à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbae5-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="cbae5-111">OS</span><span class="sxs-lookup"><span data-stu-id="cbae5-111">PARAMETERS</span></span>

### <span data-ttu-id="cbae5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbae5-112">-DefaultProfile</span></span>
<span data-ttu-id="cbae5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbae5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbae5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbae5-114">-Name</span></span>
<span data-ttu-id="cbae5-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="cbae5-115">WebApp Name</span></span>

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

### <span data-ttu-id="cbae5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbae5-116">-ResourceGroupName</span></span>
<span data-ttu-id="cbae5-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cbae5-117">Resource Group Name</span></span>

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

### <span data-ttu-id="cbae5-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="cbae5-118">-Slot</span></span>
<span data-ttu-id="cbae5-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="cbae5-119">Slot name</span></span>

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

### <span data-ttu-id="cbae5-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cbae5-120">-WebApp</span></span>
<span data-ttu-id="cbae5-121">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="cbae5-121">Piped WebApp</span></span>

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

### <span data-ttu-id="cbae5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbae5-122">CommonParameters</span></span>
<span data-ttu-id="cbae5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbae5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbae5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbae5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbae5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbae5-125">INPUTS</span></span>

### <span data-ttu-id="cbae5-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="cbae5-126">Site</span></span>
<span data-ttu-id="cbae5-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="cbae5-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cbae5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbae5-128">OUTPUTS</span></span>

### <span data-ttu-id="cbae5-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="cbae5-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="cbae5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbae5-130">NOTES</span></span>

## <span data-ttu-id="cbae5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbae5-131">RELATED LINKS</span></span>

