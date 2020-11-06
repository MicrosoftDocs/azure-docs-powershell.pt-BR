---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 0f8192441b3bf555145da8259f369a9091193800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602134"
---
# <span data-ttu-id="ad916-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="ad916-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="ad916-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad916-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad916-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad916-103">SYNTAX</span></span>

### <span data-ttu-id="ad916-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ad916-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad916-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ad916-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad916-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad916-106">DESCRIPTION</span></span>
<span data-ttu-id="ad916-107">O cmdlet **Get-AzureRmWebAppBackupList** Obtém uma lista de backups para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad916-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="ad916-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad916-108">EXAMPLES</span></span>

### <span data-ttu-id="ad916-109">1:</span><span class="sxs-lookup"><span data-stu-id="ad916-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="ad916-110">Esse comando retorna uma lista de backup relacionada a WebApp WebAppStandard associada à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad916-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="ad916-111">OS</span><span class="sxs-lookup"><span data-stu-id="ad916-111">PARAMETERS</span></span>

### <span data-ttu-id="ad916-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad916-112">-DefaultProfile</span></span>
<span data-ttu-id="ad916-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad916-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad916-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad916-114">-Name</span></span>
<span data-ttu-id="ad916-115">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="ad916-115">WebApp Name</span></span>

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

### <span data-ttu-id="ad916-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad916-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad916-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ad916-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ad916-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad916-118">-Slot</span></span>
<span data-ttu-id="ad916-119">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="ad916-119">Slot name</span></span>

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

### <span data-ttu-id="ad916-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad916-120">-WebApp</span></span>
<span data-ttu-id="ad916-121">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="ad916-121">Piped WebApp</span></span>

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

### <span data-ttu-id="ad916-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad916-122">CommonParameters</span></span>
<span data-ttu-id="ad916-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad916-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad916-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad916-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad916-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad916-125">INPUTS</span></span>

### <span data-ttu-id="ad916-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="ad916-126">Site</span></span>
<span data-ttu-id="ad916-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ad916-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ad916-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad916-128">OUTPUTS</span></span>

### <span data-ttu-id="ad916-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="ad916-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="ad916-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad916-130">NOTES</span></span>

## <span data-ttu-id="ad916-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad916-131">RELATED LINKS</span></span>

