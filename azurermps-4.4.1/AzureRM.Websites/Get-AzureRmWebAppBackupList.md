---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603071"
---
# <span data-ttu-id="6441d-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="6441d-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="6441d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6441d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6441d-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6441d-103">SYNTAX</span></span>

### <span data-ttu-id="6441d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6441d-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6441d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6441d-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6441d-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6441d-106">DESCRIPTION</span></span>
<span data-ttu-id="6441d-107">O cmdlet **Get-AzureRmWebAppBackupList** Obtém uma lista de backups para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="6441d-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="6441d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6441d-108">EXAMPLES</span></span>

### <span data-ttu-id="6441d-109">1:</span><span class="sxs-lookup"><span data-stu-id="6441d-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="6441d-110">Esse comando retorna uma lista de backup relacionada a WebApp WebAppStandard associada à ContosoResourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6441d-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="6441d-111">OS</span><span class="sxs-lookup"><span data-stu-id="6441d-111">PARAMETERS</span></span>

### <span data-ttu-id="6441d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="6441d-112">-Name</span></span>
<span data-ttu-id="6441d-113">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="6441d-113">WebApp Name</span></span>

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

### <span data-ttu-id="6441d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6441d-114">-ResourceGroupName</span></span>
<span data-ttu-id="6441d-115">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6441d-115">Resource Group Name</span></span>

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

### <span data-ttu-id="6441d-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="6441d-116">-Slot</span></span>
<span data-ttu-id="6441d-117">Nome do slot</span><span class="sxs-lookup"><span data-stu-id="6441d-117">Slot name</span></span>

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

### <span data-ttu-id="6441d-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6441d-118">-WebApp</span></span>
<span data-ttu-id="6441d-119">WebApp canalizado</span><span class="sxs-lookup"><span data-stu-id="6441d-119">Piped WebApp</span></span>

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

### <span data-ttu-id="6441d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6441d-120">-DefaultProfile</span></span>
<span data-ttu-id="6441d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6441d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6441d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6441d-122">CommonParameters</span></span>
<span data-ttu-id="6441d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6441d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6441d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6441d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6441d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6441d-125">INPUTS</span></span>

### <span data-ttu-id="6441d-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="6441d-126">Site</span></span>
<span data-ttu-id="6441d-127">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="6441d-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6441d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6441d-128">OUTPUTS</span></span>

### <span data-ttu-id="6441d-129">Microsoft. Azure. Commands. webapps. cmdlets. webapps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="6441d-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="6441d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6441d-130">NOTES</span></span>

## <span data-ttu-id="6441d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6441d-131">RELATED LINKS</span></span>

